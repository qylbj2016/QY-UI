<template>
    <div :class="['btn-wrapper', type]">
        <div class="btn">{{ text }}</div>
    </div>
</template>

<script>

import { getClassName } from "../../utils/assist" 
export default {
    props: {
			text: {
				default: '默认'
			},
			type: {
				validator( v ){
					return getClassName(v, 'btn')
				},
				type: String,
				default: 'default'
			}
    }
}
</script>


<style lang="sass" scoped>	
@import './button.sass'
</style>