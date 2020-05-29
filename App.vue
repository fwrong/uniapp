<script>
	export default {
		onLaunch: function() {
			// #ifdef H5
			uni.getSystemInfo({
				success(e){
					/* 窗口宽度大于420px且不在PC页面且不在移动设备时跳转至 PC.html 页面 */
					if(e.windowWidth>420 && !window.top.isPC && !/iOS|Android/i.test(e.system)){	
						window.location.pathname = '/static/html/pc.html';
					}
				}
			})
			// #endif
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
</style>
