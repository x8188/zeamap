<template>
    <div class="result-container">
      <el-card>
        <Title>Result</Title>
        <el-button type="primary" style="margin-bottom: 20px;" @click="returnMultiExpression()">Return</el-button>
        <div class="table-title" style="display: flex;justify-content: space-between;">
          <div class="info-nums">
           <span>show</span> 
            <el-select v-model="infoNums" placeholder="" style="width: 80px; margin: 0 8px;">
              <el-option label="123" value="123">123</el-option>
            </el-select>
            <span>results</span>
          </div>
          <button style="padding: 5px;">
            <SvgIcon icon-class="download02" color="858585"/>
            <span style="margin-left: 8px; color: #929292">Download the results</span>
          </button>
        </div>
        <div class="table-container">
          <el-table
          border
          style="width: 100%;margin-top: 30px;">
          <el-table-column
            label="Position"
          >
          </el-table-column>
          <el-table-column
            label="ID"
          >
          </el-table-column>
          <el-table-column
            label="REF">
          </el-table-column>
          <el-table-column
            label="ALT">
          </el-table-column>
          <el-table-column
            label="238">
          </el-table-column>
          <el-table-column
            label="268">
          </el-table-column>
          <el-table-column
            label="501">
          </el-table-column>
          <el-table-column
            label="1462">
          </el-table-column>
          <el-table-column
            label="4019">
          </el-table-column>
          <el-table-column
            label="5237">
          </el-table-column>
          <el-table-column
            label="5311">
          </el-table-column>
          <el-table-column
            label="7327">
          </el-table-column>
          <el-table-column
            label="7381">
          </el-table-column>
          <el-table-column
            label="9782">
          </el-table-column>
          <el-table-column
            label="526018">
          </el-table-column>
          <el-table-column
            label="CIMBL">
          </el-table-column>
        </el-table>
        </div>
      </el-card>
    </div>
</template>
<script>
import SvgIcon from '@/components/CommonComponents/SvgIcon.vue'
import Title from '@/components/CommonComponents/Title.vue'
export default {
  components: { Title, SvgIcon },
  data() {
    return {
      infoNums: 50
    }
  },
  methods: {
    returnMultiExpression() {
      this.$emit('returnMultiExpression')
    }
  }
}
</script>

<style scoped>
.result-container {
position: relative;
left: 50%;
transform: translateX(-50%);
width: 90%;
min-width: 900px;
}
</style>