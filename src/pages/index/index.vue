<template>
  <view>
    <button @click="switchTheme('Admin')">切换</button>
    <button @click="switchTheme('Empt')">切换2</button>

      <view class="common-util">
        <text>{{title}}</text>
      </view>
  </view>

</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
      switchTheme(type) {
        window.document.documentElement.setAttribute('data-theme', type)
      }
		}
	}
</script>

<style lang="scss">

@import '../../theme/handle.scss';

  .common-util {
    font-size: 18rpx;
    height: 100rpx;
    margin-top: 20rpx;
    border: 10rpx solid #ffb700;
    @include font_color('titleColor');
    @include background_color('mainColor');
    @include border_color('titleColor');
  }

	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;

    .logo {
      height: 200rpx;
      width: 200rpx;
      margin: 200rpx auto 50rpx auto;
    }

    .title {
      font-size: 36rpx;
      color: black;
    }

	}



	.text-area {
		display: flex;
		justify-content: center;
	}


</style>
