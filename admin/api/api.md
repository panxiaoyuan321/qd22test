## 登录的接口
url:api/doLogin.php
type:post
data:   email:登录的email
        password:登录的密
        
响应体
    string类型

    ok 要么 fail


## 判断是否登录的接口
url:api/checkLogin.php
type:get
data:不需要

响应体
        string

        ok 要么 fail


## 获得用户信息的接口
url:api/getUserInfo.php
type:get
data:不需要
响应体：
        JSON
        { "id":1, "slug":"admin","nickname":"管理员"..... }


## 获取网站信息的接口
url:api/getWebInfo.php
type:get
data:不需要
响应体：
        JSON
       { postsCount: 10,  draftedCount:2 , categoryCount:12, commentsCount: 3 , heldCount:4 }


## 获取所有评论数据的接口
url:api/getComments.php
type:get
data：
        pageIndex：页码，也就是说查第几页
        pageSize: 页容量,一页显示多少条
响应体：
        JSON
{
     data:[
        {"id":1,"author":"小周","content":"评论内容","title":"文章标题","created":"时间","status":"状态"},
        {},
        {}
      ],

    totalPage: 53
}