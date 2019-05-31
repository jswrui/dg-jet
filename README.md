# dg-jet
python django django-jet
创建项目
利用django-admin startproject 创建项目
下载django-jet
pip install django-jet
在setting.py中配置
INSTALLED_APPS = (
    ...
    'jet',
    'django.contrib.admin',
    ...
)

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                ...
                'django.template.context_processors.request',
                ...
            ],
        },
    },
]

在urls中配置
urlpatterns = patterns(
    '',
    url(r'^jet/', include('jet.urls', 'jet')),  # Django JET URLS
    url(r'^admin/', include(admin.site.urls)),
    ...
)

然后运行python manage.py migrate jet
其他配置可以参考
https://jet.readthedocs.io/en/latest/install.html
