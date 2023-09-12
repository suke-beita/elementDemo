<template>
  <div>
    <!-- <i class="el-icon-edit"></i>
    <br />
    <el-button class="el-icon-edit"
               type="primary"
               @click="test()"
               :loading="loading">按钮</el-button>
    <br />
    <el-link href="https://element.eleme.cn"
             icon="el-icon-edit"
             :underline="underline">Element ui</el-link>
    <br />
    <el-radio v-model="radio"
              label="1"
              @change="change">选项1</el-radio>
    <el-radio v-model="radio"
              label="2"
              @change="change">选项2</el-radio>
    <br />
    <el-checkbox :indeterminate="isIndeterminate"
                 v-model="checkAll"
                 @change="handleCheckAllChange">全选</el-checkbox>
    <div style="margin:15px 0;"></div>
    <el-checkbox-group v-model="checkedCities"
                       @change="handleCheckedCitiesChange">
      <el-checkbox v-for="city in cities"
                   :label="city"
                   :key="city">{{ city }}</el-checkbox>
    </el-checkbox-group>
    <br />
    <el-input v-model="input"
              placeholder="请输入"></el-input>
    <el-button @click="click"
               type="primary">提交修改</el-button>
    <br />
    <el-select v-model="value"
               placeholder="请选择"
               @change="change2">
      <el-option v-for="item in options"
                 :label="item.label"
                 :key="item.value"
                 :value="item.value"
                 :disabled="item.disabled"></el-option>
    </el-select> -->
    <!-- <el-switch v-model="value"
               active-color="#13ce66"
               active-text="上架"
               inactive-color="#ff4949"
               inactive-text="下架"
               @change="change"></el-switch> -->
    <!-- <el-form ref="form"
             :model="form"
             :rules="rules"
             label-width="80px">
      <el-form-item label="活动名称"
                    prop="name">
        <el-input v-model="form.name"></el-input>
      </el-form-item>
      <el-form-item label="活动区域"
                    prop="region">
        <el-select v-model="form.region"
                   placeholder="请选择活动区域">
          <el-option label="区域一"
                     value="shanghai"></el-option>
          <el-option label="区域二"
                     value="beijing"></el-option>
        </el-select>
      </el-form-item> -->
    <!-- <el-form-item label="活动时间">
        <el-col :span="11">
          <el-date-picker type="date"
                          placeholder="选择日期"
                          v-model="form.date1"
                          style="width: 100%;"></el-date-picker>
        </el-col>
        <el-col class="line"
                :span="2">-</el-col>
        <el-col :span="11">
          <el-time-picker placeholder="选择时间"
                          v-model="form.date2"
                          style="width: 100%;"></el-time-picker>
        </el-col>
      </el-form-item> -->
    <!-- <el-form-item label="即时配送"
                    prop="delivery">
        <el-switch v-model="form.delivery"></el-switch>
      </el-form-item>
      <el-form-item label="活动性质"
                    prop="type">
        <el-checkbox-group v-model="form.type">
          <el-checkbox label="美食/餐厅线上活动"
                       name="type"></el-checkbox>
          <el-checkbox label="地推活动"
                       name="type"></el-checkbox>
          <el-checkbox label="线下主题活动"
                       name="type"></el-checkbox>
          <el-checkbox label="单纯品牌曝光"
                       name="type"></el-checkbox>
        </el-checkbox-group>
      </el-form-item>
      <el-form-item label="特殊资源"
                    prop="resource">
        <el-radio-group v-model="form.resource">
          <el-radio label="线上品牌商赞助"></el-radio>
          <el-radio label="线下场地免费"></el-radio>
        </el-radio-group>
      </el-form-item> -->
    <!-- <el-form-item label="活动形式">
        <el-input type="textarea"
                  v-model="form.desc"></el-input>
      </el-form-item> -->
    <!-- <el-form-item>
        <el-button type="primary"
                   @click="onSubmit('form')">立即创建</el-button>
        <el-button @click="resetForm('form')">取消</el-button>
      </el-form-item>
    </el-form> -->
    <!-- <el-form ref="form"
             :model="form"
             :rules="rules"
             label-width="80px">
      <el-form-item label="邮箱"
                    prop="email">
        <el-input v-model="form.email"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary"
                   @click="onSubmit('form')">立即创建</el-button>
        <el-button @click="resetForm('form')">取消</el-button>
      </el-form-item>
    </el-form> -->
    <el-form ref="form"
             :model="form"
             :rules="rules"
             label-width="80px">
      <el-form-item label="年龄"
                    prop="age"
                    :rules="[
                      { required: true, message: '年龄不能为空', trigger: 'blur' },
                      { type:'number', message: '年龄必须位数字', trigger: 'blur' }
                    ]">
        <el-input v-model.number="form.age"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary"
                   @click="onSubmit('form')">立即创建</el-button>
        <el-button @click="resetForm('form')">取消</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
// const cityOptions = ["北京", "上海", "广州", "深圳"];
export default {
  methods: {
    // click () {
    //   this.input = 'abc'
    // },
    // test () {
    //   this.loading = true;
    //   setTimeout(() => {
    //     this.loading = false
    //   }, 3000)
    // },
    // change () {
    //   console.log('当前radio的值是：' + this.radio)
    // },
    // change2 () {
    //   console.log('当前选中的是' + this.value)
    // },
    // handleCheckAllChange (val) {
    //   this.checkedCities = val ? cityOptions : [];
    //   this.isIndeterminate = false;
    // },
    // handleCheckedCitiesChange (value) {
    //   //当前选中的数量
    //   let checkedCount = value.length;
    //   this.checkAll = checkedCount === this.cities.length;
    //   this.isIndeterminate = checkedCount > 0 && checkedCount < this.cities.length
    // }
    // change () {
    //   console.log('当前开关的状态是' + this.value)
    // }
    onSubmit (formName) {
      this.$refs[formName].validate((valid) => {
        if (valid) {
          alert('submit!');
        } else {
          console.log('error submit!!');
          return false;
        }
      });
    },
    resetForm (formName) {
      this.$refs[formName].resetFields();
    }
  },
  data () {
    var checkEmail = (rule, value, callback) => {
      const mailReg = /^([a-zA-Z0-9_-])+@([a-zA-Z0-9_-])+(.[a-zA-Z0-9_-])+/
      if (!value) {
        return callback(new Error('邮箱不能为空'))
      }
      setTimeout(() => {
        if (mailReg.test(value)) {
          callback()
        } else {
          callback(new Error('邮箱格式错误'))
        }
      }, 100)
    };
    return {
      // loading: false,
      // underline: false,
      // radio: "1",//默认选中
      // checkAll: false,
      // checkedCities: ['上海', '北京'],
      // cities: cityOptions,
      // isIndeterminate: true,
      // input: '',
      // options: [
      //   {
      //     value: '1',
      //     label: '蛋糕',
      //     disabled: true
      //   },
      //   {
      //     value: '2',
      //     label: '面包'
      //   },
      //   {
      //     value: '3',
      //     label: '鸡蛋'
      //   },
      // ],
      // value: ''
      // value: ''//除了true，全认为是false
      form: {
        age: '',
        // email: '',
        // name:'',
        // region: '',
        // date1: '',
        // date2: '',
        // delivery: false,
        // type: [],
        // resource: '',
        // desc: ''
      },
      rules: {
        email: [
          // { required: true, message: '请输入活动名称', trigger: 'blur' },
          // { min: 3, max: 5, message: '长度在 3 到 5 个字符', trigger: 'blur' }
          { required: true, validator: checkEmail, message: '请输入邮箱', trigger: 'blur' },
        ],
        // region: [
        //   { required: true, message: '请选择活动区域', trigger: 'change' }
        // ],
        // date1: [
        //   { type: 'date', required: true, message: '请选择日期', trigger: 'change' }
        // ],
        // date2: [
        //   { type: 'date', required: true, message: '请选择时间', trigger: 'change' }
        // ],
        // type: [
        //   { type: 'array', required: true, message: '请至少选择一个活动性质', trigger: 'change' }
        // ],
        // resource: [
        //   { required: true, message: '请选择活动资源', trigger: 'change' }
        // ],
        // desc: [
        //   { required: true, message: '请填写活动形式', trigger: 'blur' }
        // ]
      }
    }
  }
}
</script>

<style>
</style>