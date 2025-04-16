<script setup>
import { useI18n } from 'vue-i18n'
import { useGlobalState } from '../store'
const { openSettings } = useGlobalState()


const { t } = useI18n({
    messages: {
        en: {
            copyright: "Copyright"
        },
        zh: {
            copyright: "版权所有"
        }
    }
});

</script>

<template>
    <!-- <div>
        <n-divider class="footer-divider" />
        <div style="text-align: center; padding: 20px">
            <n-space justify="center">
                <n-text depth="3">
                    {{ t('copyright') }} © 2023-{{ new Date().getFullYear() }}
                </n-text>
                <n-text depth="3">
                    <div v-html="openSettings.copyright"></div>
                </n-text>
            </n-space>
        </div>
    </div> -->
    <footer>
      <div style="padding: 20px;">
        <div style="text-align: center;">
          <div style="color: black;"> © 
            <a  style="color: black; text-decoration: none;" href="https://beian.miit.gov.cn/" target="_blank"> 冀ICP备17000836号-2 </a>
          </div>
        </div>
        <div style="text-align: center;">
          <div style="color: black;">
            <img src="//cdn.smallyoung.cn/libs/image/beian.png" alt="冀公网安备 13018102000160号" style="vertical-align:middle;">
            <a style="color: black;text-decoration: none;" target="_blank" href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=13018102000160">冀公网安备
              13018102000160号</a>
          </div>
        </div>
      </div>
    </footer>
</template>


<style scoped>
.footer-divider {
    margin: 0;
    padding: 0 var(--x-padding);
}
</style>
