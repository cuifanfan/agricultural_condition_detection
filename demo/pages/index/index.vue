<template>
	<view class="container">
		<view class="header">
			<view class="title center">
				<text>茶园种植</text>
			</view>

			<view class="navbar">
				<uni-row>
					<uni-col v-for="(nav, index) in navs" :key="index" :span="6">
						<view class="nav text u-flex">
							<view class="nav_icon">
								<uni-icons custom-prefix="iconfont" :type="nav.icon" size="22" color="#2dc590">
								</uni-icons>
							</view>
							<text>{{nav.text}}</text>
						</view>
					</uni-col>
				</uni-row>
			</view>

			<view class="message">
				<view class="tip px angle_content u-flex">
					<view>
						<uni-icons type="sound" size="19" color="#949699"></uni-icons>
						<text class="text_pl gray_color ">暂无消息！</text>
					</view>
					<view>
						<uni-icons type="right" size="15" color="#949699"></uni-icons>
					</view>
				</view>
			</view>
		</view>

		<view class="content">
			<uni-card :is-shadow="false" class="angle_content pb">
				<template v-slot:title>
					<view class="content_toolbar u-flex ">
						<view>
							<uni-icons custom-prefix="iconfont" type="icon-ditu" size="15" color="#949699"></uni-icons>
							<text class="gray_color content_toolbar_left">老班章</text>
							<uni-icons type="right" size="15" color="#949699"></uni-icons>
						</view>
						<view>
							<uni-icons type="gear" size="15" color="#949699"></uni-icons>
							<text class="text_pl">设备</text>
						</view>
					</view>
				</template>

				<view>
					<uni-row class="u-flex">
						<uni-col :span="8">
							<view class="content_garden_left text center">5000</view>
							<view class="text center">茶园面积</view>
						</uni-col>
						<uni-col :span="8">
							<view class="content_garden_center center">1</view>
							<view class="text center">茶园数量</view>
						</uni-col>
						<uni-col :span="8">
							<view class="content_garden_right center">饼圆茶、古树茶</view>
							<view class="text center">种植品类</view>
						</uni-col>
					</uni-row>
				</view>

				<view slot="actions" class="conten_environment">
					<view class="u-flex">
						<view class="text">
							<text class="content_temperature_number">21.8</text>°C
						</view>
						<view class="content_cloud">
							<text>多云</text>
							<uni-icons custom-prefix="iconfont" type="icon-duoyun" size="20" color="#c9dfff"
								class="text_pl"></uni-icons>
						</view>
					</view>
					<view class="conten_environment_condition">
						<uni-row class="mt">
							<uni-col :span="12">
								<view class="condition_details">
									<view class="condition-icon ">
										<uni-icons custom-prefix="iconfont" type="icon-fengshan" size="25"
											color="#3675d5">
										</uni-icons>
									</view>
									<view class="ml">
										<view><text class="condition_number">1</text>级</view>
										<view class="text">风力</view>
									</view>
								</view>
							</uni-col>
							<uni-col :span="12">
								<view class="condition_details">
									<view class="condition-icon ">
										<uni-icons custom-prefix="iconfont" type="icon-fengsu" size="25"
											color="#3675d5">
										</uni-icons>
									</view>
									<view class="ml">
										<view><text class="condition_number">0.9</text>m/s</view>
										<view class="text">风速</view>
									</view>
								</view>
							</uni-col>
						</uni-row>

						<uni-row class="mt">
							<uni-col :span="12">
								<view class="condition_details">
									<view class="condition-icon">
										<uni-icons custom-prefix="iconfont" type="icon-tianqi-fengxiang" size="25"
											color="#3675d5">
										</uni-icons>
									</view>
									<view class="ml">
										<view><text class="condition_number">西风</text></view>
										<view class="text">风向</view>
									</view>
								</view>

							</uni-col>
							<uni-col :span="12">
								<view class="condition_details">
									<view class="condition-icon ">
										<uni-icons custom-prefix="iconfont" type="icon-jianzhuanquan" size="25"
											color="#3675d5">
										</uni-icons>
									</view>
									<view class="ml">
										<view><text class="condition_number">21.8</text>°C</view>
										<view class="text">空气温度</view>
									</view>
								</view>
							</uni-col>
						</uni-row>
						<uni-row class="mt">
							<uni-col :span="12">
								<view class="condition_details">
									<view class="condition-icon ">
										<uni-icons custom-prefix="iconfont" type="icon-duoyun" size="25"
											color="#3675d5">
										</uni-icons>
									</view>
									<view class="ml">
										<view><text class="condition_number">30.3</text>%RH</view>
										<view class="text">空气湿度</view>
									</view>
								</view>
							</uni-col>
							<uni-col :span="12">
								<view class="condition_details">
									<view class="condition-icon ">
										<uni-icons custom-prefix="iconfont" type="icon-pm" size="25" color="#3675d5">
										</uni-icons>
									</view>
									<view class="ml">
										<view><text class="condition_number">1</text>ug/m3</view>
										<view class="text">Pm2.5</view>
									</view>
								</view>
							</uni-col>
						</uni-row>
						<uni-row class="mt">
							<uni-col :span="12">
								<view class="condition_details">
									<view class="condition-icon ">
										<uni-icons custom-prefix="iconfont" type="icon-yibiaopan" size="25"
											color="#3675d5">
										</uni-icons>
									</view>
									<view class="ml">
										<view><text class="condition_number">81.8</text>kpa</view>
										<view class="text">大气压</view>
									</view>
								</view>
							</uni-col>
							<uni-col :span="12">
								<view class="condition_details">
									<view class="condition-icon ">
										<uni-icons custom-prefix="iconfont" type="icon-duoyun" size="25"
											color="#3675d5">
										</uni-icons>
									</view>
									<view class="ml">
										<view><text class="condition_number">41007</text>lux</view>
										<view class="text">光照</view>
									</view>
								</view>
							</uni-col>
						</uni-row>
					</view>
				</view>
			</uni-card>

		</view>
	</view>

</template>

<script>
	export default {
		data() {
			return {
				navs: [{
					text: '农情监测',
					icon: 'icon-tiaopinjiance'
				}, {
					text: '智能控制',
					icon: 'icon-31shezhi'
				}, {
					text: '农业知识库',
					icon: 'icon-zhishiku'
				}, {
					text: '专家问诊',
					icon: 'icon-chongwuwenzhen'
				}]
			}
		},

	}
</script>

<style>
	@import "@/static/css/base.css";
	@import "@/static/css/index.css"
</style>
