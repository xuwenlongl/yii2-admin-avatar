Avatar Upload
=============
Avatar Upload

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist xwl/yii2-avatar "*"
```

or add

```
"xwl/yii2-avatar": "*"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
//在当前控制器的actions中添加如下配置
public function actions()
{
    return [
        'crop'=>[
            'class' => 'hyii2\avatar\CropAction',
            'config'=>[
                'bigImageWidth' => '200',     //大图默认宽度
                'bigImageHeight' => '200',    //大图默认高度
                'middleImageWidth'=> '100',   //中图默认宽度
                'middleImageHeight'=> '100',  //中图图默认高度
                'smallImageWidth' => '50',    //小图默认宽度
                'smallImageHeight' => '50',   //小图默认高度
                
                //头像上传目录（注：目录前不能加"/"）
                'uploadPath' => 'uploads/avatar',
            ]
        ]
    ]; 
    
}

<?= \xwl\avatar\AutoloadExample::widget(); ?>

```