<template>
  <nav text-xl mt-6 inline-block gap-2>
    <el-row>
      <el-button type="info" plain @click="go('/fish')">待钓列表</el-button>
      <el-button type="info" plain @click="go('/Accomplishment')">成就</el-button>
      <button icon-btn @click="toggleDark()">
        <div dark:i-carbon-moon i-carbon-sun />
      </button>
    </el-row>

    <el-row text-sm>
      <el-progress
      class="w200px h20px"
      :show-text="false"
      :percentage="50"
    />
      <p>泰瑞亚时间</p>
    </el-row>
    
    <el-row text-sm>
      <el-progress
      class="w200px h20px"
      :show-text="false"
      :percentage="50"
    />
    <p>凯珊时间</p>
    </el-row>
    
  </nav>
</template>

<script setup lang="ts">

const router = useRouter()
const go = (link: string) => {
  router.push(link)
}
</script>