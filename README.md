# FBData
 Aplicação Web para divulgação de portfolio de Dashboard com aplicativo PowerBI 

 ### Lista de tarefas
Segue a lista de tarefas a serem desenvolvidas no projeto:
- [X] Pré-requisitos
    - [X] Instalar o Python
    - [X] Instalar Visual Studio Code
- [X] Criar e ativar ambiente visual
``` 
python -m venv .\venv\
venv\Scripts\activate
```
- [X] Instalar o Django
``` 
python -m pip install django==3.2
python -m pip freeze 
```
- [X] Criar o projeto personalCheff
```
django-admin.py startproject PersonalCheffProj
```
- [X] Subir o servidor e testar o projeto
``` 
Entrar na pasta do projeto 
cd PersonalCheffProj

Executar o projeto no servidor
python manage.py runserver
```

- [X] Alterar o idioma do projeto para `pt-br`
```
Linha 106 da settings.py LANGUAGE_CODE = 'pt-br'
```
- [X] Alterar o timezone do projeto para `America/São_Paulo`
```
Alterado a time zone no settings.py para America_Sao_Paulo.
Link para time zone 'list of pytz time zones · GitHub'
```
- [X] Criar o app receitas
```
*Preciso estar dentro da pasta do projeto (PeronalCheffProj) 
python manage.py startapp receitas
```
- [X] Registrar o app receitas
```
no arquivo setting.py adicionar o app receitas na lista de app INSTALED APP
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'receitas' ,
```
- [ ] Configurar a rota inicial (index)
```
Criar uma pasta urls dentro de receitas 

from django.urls import path
from.import views
urlpatterns = [
    path('', views.index,name= 'index')
    
```
- [ ] Registrar a rota inicial
    - Dentro da pasta PersonalCheffProj (app) abrir o arquivo 'urls.py'
    '''python
    from django.contrib import admin
    from django.urls import path, include

    urlpatterns = [
        path('admin/', admin.site.urls)
        path('', include('receitas.urls'))
    ]

- [ ] Criar o arquivo index.html 

