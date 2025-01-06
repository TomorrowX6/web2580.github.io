<template>
  <q-page class="column flex-center">

  萝莉先辈曲国强是一名大學生，大学时最喜欢的运动是看着萝莉打胶<br>每天都化身成坏叔叔去抓小萝莉<br>去年曾因诱骗萝莉被他人举报，入狱劳改<br>却因其是天才黑客攻破美国国防系统而减刑，每日在指定地点工作改造<br>因其高超的摸🐟技巧和强大的工作能力，工作很本不是问题<br>因此每日空闲时间就会看萝莉本子和制作与萝莉幸福生活的Galgame<br>以下是萝莉先辈的代表作品
    <div class="q-mt-md">
      <q-toggle
        :model-value="$q.dark.isActive"
        :checked-icon="symRoundedDarkMode"
        :unchecked-icon="symRoundedLightMode"
        size="xl"
        @update:model-value="$q.dark.toggle()"
      />
    </div>
  </q-page>
</template>

<script setup>
import {
  symRoundedDarkMode,
  symRoundedLightMode,
} from '@quasar/extras/material-symbols-rounded';
import { Dark } from 'quasar';
import { computed, ref } from 'vue';

import innerLogoDark from 'assets/quasar-logo-inner-dark.svg';
import innerLogoLight from 'assets/quasar-logo-inner-light.svg';
import verticalLogoDark from 'assets/quasar-logo-vertical-dark.svg';
import verticalLogoLight from 'assets/quasar-logo-vertical-light.svg';

const innerLogo = computed(() =>
  Dark.isActive ? innerLogoDark : innerLogoLight,
);

const verticalLogo = computed(() =>
  Dark.isActive ? verticalLogoDark : verticalLogoLight,
);

</script>
