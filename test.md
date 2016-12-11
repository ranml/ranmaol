# 1
```
主要方向：前段，导师：刘荣博
         后端，导师：吴培楠
```
# 2
```php
<?php
$arr1 = array("color"=>"red",2,4);
$arr2 =array("a","b","color"=>"green","shape"=>"trapezoid",4);
$result =array_merge($arr1,$arr2);


function merge($arr1, $arr2){
    $arr = [];
 return array_merge($arr1,$arr2);
    foreach($arr1 as $k=>$v){
        $arr[$k] = $v;
    }
   
}
   

$arr = merge($arr1, $arr2);

print_r($arr);
```


# 3. 校园博客平台数据库建立
## 3.1 & 3.2
```sql
#
create database blog

 # 用户表
create table User_rml(userID char(15) not null,
                  userName char(10) not null,
                  passWord char(10) not null,
                  name char(10)not null,
                  phoneNumber char(11) not null);

# 游客表:
create table visitor_rml(ID char(15) not null,
                  userName char(10) not null,
                 articleID char(10) not null);

# 
create table blog_rml(articleID char(10) not null,
                  title char(10) not null,
                  articleType char(10) not null,
                  articleCon text not null,
                  submitTime date not null,
                  prideNum int not null,
                  userID  char(15) not null);
```
## 3.3
```sql
 select title,articleType,articleCon,submitTime,prideNum,userName 
 from User_rml,blog_rml
 where blog_rml.userID=User_rml.userID;
```
# 4.获取ul元素
## li实现
```js
var ul = document.querySelector("ul");
var myFun = function(){}
for(var i=0; i<5000; i++){
    var li =  document.createElement("li");
        li.onclick =  myFun;
        ul.appendChild(li);
}
```
# 5.请求当前目录的文件。
js.ajax
## 5.1
处理服务器响应后返回的结果（根据http状态码）。
## 5.2（选做题）
不能。
# 6 数据库查询语句
```sql

    select * from students where id<4;
    select username,stuld from students where id  like '2015210%';
    select * from students where username like '%明%';

```
# 7 写出代码输出内容
```php
Class A...
Class B...

```


# 8 保证数组中元素的不重复性
```js
var arr = [1, 2, 3, 3, 4,4, 5, 6];
var temp = [];
for(var i=0; i<arr.length; i++){
    if(temp.indexOf(arr[i]) == -1){
        temp.push(arr[i]);
    } 
}
console.log(temp);
```
# 9  输出值
```js

`aaaaa`和`aaaaa`
```
# 10 前后端，服务器的协调 
```
前端写入数据，通过http协议运输，然后php程序由此得到数据到后端，即后端进行处理。

````
# 11 输出arr的值
```
arr[1]()=  > 
arr[2]()=  >
```

# 12 男票的自我介绍
```php
<?php
class Person
{
    public $name;
    public $sex;
    public $age;
    public $height;
    public $temperament;
}
interface Introduction
{
    function introduce();
}
class BoyFriend extends Person implements Introduction{
   var $weight;
    public function  __construct($name, $sex,$age,$height,$weight,$temperament){
       $this->weight = $weight;
       $this->name = $name;
       $this->sex=$sex;
       $this->age=$age;
       $this->height=$height;
       $this->temperament=$temperament;
    }
    public function introduce(){
         echo "我的名字是".$this->name.
         "，性别是".$this->sex.
         "，身高是".$this->height.",体重是".$this->weight."，年龄".$this->age;

    }
}

$b =new BoyFriend("张华", "男",180,130,21);

$b->introduce();
```
# 13(1)
```js
-->
```
# 13(2) 
```js
var ul = document.getElementById("target");
var li = ul.getElementsByTagName("li");
 li.reverse();
```
# 14 canvas
```canvas
两种：
 创建 Canvas 元素 向 HTML5 页面添加 canvas 元素
 创建 context 对象
```
# 15 用php写一个函数
```php

<?php
$arr1 = array("color"=>"red",2,4);
$arr2 =array("a","b","color"=>"green","shape"=>"trapezoid",4);gf
function array_key($arr, $key = ""){
    $temp = [];
     $i = 0;   
     foreach($arr as $k=>$v){    
        if($key == ""){
           
            $temp[$i] = $k;
        }else{
            if($key == $v){
                $temp[$i] = $k;
            }
        }
        $i++;
    }

    return $temp;

}

$as = array_key($arr2);

print_r($as);
```
# 16 更改代码
```js and php
if($password==$result['password'] and $username==$result['username']){
echo="1";
}
else{
    echo="0";
}
var username, password, login, res;

username = document.getElementById("username");
password = document.getElementById("password");
login = document.getElementById("login");
res = document.getElementById("res");



var xhr = new XMLHttpRequest();

xhr.open("POST", "doAction.php", true);
xhr.setRequestHeader("Content-type","application/x-www-form-urlencoded");
xhr.onreadystatechange = function(){
    var XMLHttpReq = xhr;
    if (XMLHttpReq.readyState == 4) {
        if (XMLHttpReq.status == 200) {
            var text = XMLHttpReq.responseText;
            if(text == "0"){
                alert("用户名或密码错误！");
            }else{
                alert("登录成功");
            }
        }
    }
};
```




