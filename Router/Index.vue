<script>

import { createRouter, createWebHistory } from 'vue-router'
import Home from '~/pages/index.vue'
import Technology from '~/pages/Technology.vue'
import Projects from '~/pages/Projects.vue'
import Company from '~/pages/Company.vue'
import Career from '~/pages/Career.vue'
import Contact from '~/pages/Contact.vue'

export default defineNuxtPlugin((nuxtApp) => {
  const base = import.meta.env.BASE_URL || '/shreeom_website/'

  const router = createRouter({
    history: createWebHistory(base),
    routes: [
      { path: '/', component: Home },
      { path: '/technology', component: Technology },
      { path: '/projects', component: Projects },
      { path: '/company', component: Company },
      { path: '/career', component: Career },
      { path: '/contact', component: Contact },
    ],
  })

  nuxtApp.vueApp.use(router)
})

</script>