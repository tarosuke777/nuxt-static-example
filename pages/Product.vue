<template>
  <h2>{{ title }}</h2>
</template>

<script>
export default {
  async asyncData (context) {
    return await new Promise(resolve => {
      // バックエンドからのデータ取得をエミュレート
      setTimeout(() => {
        resolve({
          title: `このページはNuxt社のプロダクトページです。(${context.isServer ? 'サーバサイドレンダリング' : 'クライアントサイドレンダリング'})`
        })
      }, 1000)
    })
  } 
}
</script>
