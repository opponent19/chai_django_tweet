# chai_django_tweet

1. create env 
2. pip install django
3. requirements.txt  pip freeze > requirements.txt
4. django-admin startproject <project name> 
5. create super user    python manage.pr createsuperuser
<username>
<email>
<password>
(env) mahendrayadav@Mahendras-MacBook-Air chaiheadq % python manage.py createsuperuser
Username (leave blank to use 'mahendrayadav'): mahendra_chai_tweew
Email address: yadavitmahendra@gmail.com
Password: Opponent@111
Password (again): Opponent@111
Superuser created successfully.

6. media configration in settings.py
    import os


    MEDIA_URL = '/media/'
    MEDIA_ROOT = os.path.join(BASE_DIR, 'media')

    STATIC_URL = 'static/'
    STATICFILES_DIRS = [os.path.join(BASE_DIR, 'static')]

7. update urls.py

    from django.contrib import admin
    from django.urls import path
    from django.conf import settings
    from django.conf.urls.static import static


    urlpatterns = [
        path('admin/', admin.site.urls),
    ] + static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)

8. 