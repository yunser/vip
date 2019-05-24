<template>
    <my-page title="VIP" :page="page">
        <div class="common-container container">
            <ui-article>
                <h2>VIP 特权</h2>
                <ul>
                    <li>更大存储。拥有更大的云盘存储空间。</li>
                    <li>身份铭牌。在聊天、评论等地方的昵称旁会显示 VIP 标志，让你更加与众不同。</li>
                    <li>VIP 服务。拥有你的专属客服，遇到问题，可以一对一解决。</li>
                </ul>
            </ui-article>
            <ui-raised-button secondary label="升级 VIP" @click="getVip" />
        </div>
    </my-page>
</template>

<script>
    /* eslint-disable */
    import oss from '@/util/oss'
    const moment = window.moment

    export default {
        data () {
            return {
                page: {
                    menu: [
                        {
                            type: 'icon',
                            icon: 'apps',
                            href: 'https://app.yunser.com?utm_source=message',
                            to: 'xxx',
                            target: '_blank',
                            title: '应用'
                        }
                        // {
                        //     type: 'icon',
                        //     icon: 'list',
                        //     to: '/balanceIos',
                        //     title: '收支'
                        // },
                    ]
                }
            }
        },
        mounted() {
            this.loadData()
        },
        methods: {
            getVip() {
                this.$message({
                    type: 'info',
                    text: '功能暂时不可用，请联系客服'
                })
            }
        },
        filters: {
        }
    }
</script>

<style lang="scss" scoped>
.user-list {
    .item {
        margin-bottom: 16px;
        border: 1px solid rgba(0, 0, 0, .12);
    }
    .link {
        display: flex;
        padding: 16px;
    }
    .name {
        font-size: 20px;
        font-weight: bold;
    }
    .avatar {
        width: 56px;
        height: 56px;
        margin-right: 8px;
        border-radius: 4px;
    }
}
.simple-login-box {
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, .12);
}
.container {
    padding: 16px 0 80px 0;
    max-width: 400px;
}
.section—title {
    font-size: 24px;
    margin: 16px 0;
}
.quick-list {
    display: flex;
    flex-wrap: wrap;
    .item {
        padding: 4px 8px;
        margin-right: 8px;
        margin-bottom: 8px;
        border: 1px solid #000;
        cursor: pointer;
    }
}
.group-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 8px 16px;
    background-color: #f1f1f1;
    .group-in {
        margin-left: 8px;
    }
}
.total {
    padding: 0 16px;
    margin-bottom: 16px;
    .total-in {
        margin-right: 16px;
    }
}
.record-list {
    .item {
        // display: flex;
        // justify-content: space-between;
        padding: 8px 16px;
        border-bottom: 1px solid rgba(0, 0, 0, .12);
    }
    .link {
        display: flex;
        justify-content: space-between;
        color: inherit;
    }
    .name {
        font-size: 16px;
        font-weight: bold;
        cursor: pointer;
    }
    .times {
        color: #666;
        cursor: pointer;
    }
    .note {
        color: #999;
    }
    .number {
        text-align: right;
    }
    .balance {
        // color: #f00;
        text-align: right;
    }
    .balance-1 {
        color: rgb(34, 201, 48);
    }
    .balance-2 {
        color: #f00;
    }
}
.float-button {
    position: fixed;
    right: 24px;
    bottom: 24px;
}
.float-button2 {
    position: fixed;
    left: 24px;
    bottom: 24px;
}
.sign {
    margin-bottom: 8px;
}
.empty {
    .text {
        color: #999;
        padding: 80px 0;
        text-align: center;
    }
}
.search-box {
    display: flex;
    width: 100%;
    max-width: 100%;
    margin-bottom: 24px;
    // border: 1px solid #eee;
    box-shadow: 0 1px 6px rgba(0,0,0,.117647), 0 1px 4px rgba(0,0,0,.117647);
    background-color: #fff;
    &:hover {
        box-shadow: 0 3px 8px 0 rgba(0,0,0,0.2), 0 0 0 1px rgba(0,0,0,0.08);
    }
    .input {
        flex-grow: 1;
        display: block;
        height: 48px;
        padding: 0 16px;
        line-height: 48px;
        border: none;
        outline: none;
    }
}
</style>
