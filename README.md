# simpletodo
基于django的一个个人博客系统，包含首页，文章详情，文章归档，标签云和评论等，支持登陆和注册。

## 环境

        python 2.7.6
        django 1.8.3
        MySQL-python 1.2.5
        pillow 2.3.0

## 使用方法

> ### 克隆到本地

```sh
git clone git@github.com:airborne007/django-blog.git
```

> ### 修改setting中数据库配置为你自己的配置

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'davidblog',
        'USER': 'root',
        'PASSWORD': 'password',
        'HOST': '',
        'PORT': '3306',
    }
}
```
先在mysql中创建数据库`davidblog`，或者改为任何你喜欢的名字，
然后将`DATABASES`配置改为你自己的配置。

> ### 同步数据库

```sh
$ python manage.py makemigrations
$ python manage.py migrate
```

如果需要创建超级管理用户，再运行

```sh
$ python manage.py createsuperuser
```

> ### 运行

```sh
$ python manage.py runserver
```

之后在浏览器打开[http://127.0.0.1:8000](http://localhost:8000)，即可看到blog页面。
