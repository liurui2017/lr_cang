<template>
    <div>
        <cube-form
                :model="model"
                :schema="schema"
                @submit="submitHandler"
        ></cube-form>
    </div>
</template>
<script>
    export default {
        data(){
            return {
                schema:{
                    model:{
                        username:'',
                        password:''
                    },
                    filds:[
                        // usrname
                        {
                            type:'input',
                            label:'用户名',
                            rules:{
                                type:{
                                    string,
                                    number,
                                    tel,
                                    email
                                }
                            },
                            message:{
                                required:''
                            }
                        }
                    ]
                }
            }
        }
    }
</script>
<style lang="stylus" scoped>

</style>
