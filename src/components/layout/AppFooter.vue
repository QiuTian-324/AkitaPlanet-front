<script setup>
import { storeToRefs } from 'pinia'
import { useAppStore } from '@/store'

const { blogInfo } = storeToRefs(useAppStore())
</script>

<template>
  <footer class="f-c-c">
    <div class="footer-wrap w-full px-5 py-2 text-center text-white leading-8">
      <p> &copy;{{ 2024 }} - {{ new Date().getFullYear() }} akita</p>
      <a href="https://beian.miit.gov.cn/" target="_blank">
        {{ blogInfo.blog_config?.website_record }}
      </a>
    </div>
  </footer>
</template>

<style scoped>
.footer-wrap {
  background: #7dd77d;
  background-size: 400% 400%;
  animation: Gradient 8s ease infinite;
}

@keyframes Gradient {
  0% {
    background-position: 0 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0 50%;
  }
}
</style>
