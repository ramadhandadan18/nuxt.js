<template >
  <div id="wrapper">
	  <app-sidebar v-if="show"></app-sidebar>
	    <!-- Content Wrapper -->
        <div id="content-wrapper" class="d-flex flex-column">
            <!-- Main Content -->
            <div id="content">
				<app-header v-if="show"></app-header>
    			<Nuxt />
			</div>
			<app-footer v-if="show"></app-footer>
		</div>
  </div>
</template>

<script>
	import Sidebar from '@/components/layouts/Sidebar.vue'
	import Header from '@/components/layouts/Header.vue'
	import Footer from '@/components/layouts/Footer.vue'
	export default {
		data(){
			return{ show:false
			}		
		},
		computed:{
		},
		components:{
			'app-sidebar' : Sidebar,
			'app-header' : Header,
			'app-footer' : Footer
		}
	}
</script>