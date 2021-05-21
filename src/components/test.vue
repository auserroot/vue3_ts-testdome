<template>
	<div>
		<button @click="headleClick">{{ count }}</button>
	</div>
</template>

<script lang="ts">
import { ref , onMounted} from 'vue';
export default {
	setup() {
		const count:any = ref(0); //双向绑定数据、初始化值
		// console.log(count)//RefImpl 对象
		const headleClick:any = () => {
			count.value++//取值自增
		};
		
		onMounted(()=>{
			setInterval(()=>{
				headleClick()
			},1000)
		})
		return {
			count,
			headleClick
		};
	},
	
};
</script>

<style></style>
