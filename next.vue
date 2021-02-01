<template>
    <div class="pop-wrap" v-if="isShow">
        <div class="pop-bgm"></div>
        <div class="pop-content" :class="`style_${active}`">
            <img :src="`https://qwe.ewq.com/${active}`" />
            <button @click="goNext(active+1)">继续探索</button>
            <button @click="hidePop">跳过</button>
        </div>
    </div>
</template>
<script>
export default {
    data () {
        return {
            active: 0,
            isShow: true
        };
    },
    methods: {
        goNext (index) {
            if (index === 6) {
                this.isShow = false;
                return;
            }
            this.active = index;
        },
        hidePop () {
            this.isShow = false;
        }
    }
};
</script>
<style >
.style_0 {
}
.style_1 {
    
}
.style_2 {
    
}
.style_3 {
    
}
.style_4 {
    
}
.style_5 {
    
}
</style>