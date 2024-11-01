# ⚙️ Instalação padrão do Django (PT-BR)

Este arquivo instrui sobre a instalação padrão do Framework Django, inicialização de um projeto e também inicialização de um aplicativo.  

### Tópicos:  
- [Instalação](#instalação)
- [Inicialização de um projeto](#inicialização-de-projeto)
- [Inicialização de um aplicativo](#inicialização-de-aplicativo)
---
### Recomendações:  
- Atualização do gerenciador de pacotes padrão do python `pip`.
- Utilização de máquina virtual para evitar conflitos com outras bibliotecas instaladas no computador.
---
### Instruções:
- Caso precise de instruções para atualizar gerenciador de pacotes, acesse:  
[Gerenciador de Pacotes](pip.md)

- Caso precise de instruções para configurar a máquina virtual, acesse:  
[Máquina Virtual](virtual_env.md)
---

### Instalação
Após ativar a máquina virtual, faça a instalação do Django:
```powershell
# Comando para instalação do django
pip install django

# Caso queira instalar uma versão específica
pip install django==3.2
```
---

Verifique se a instalação foi bem sucedida:
```powershell
# Comando para verificar a instalação do Django
django-admin --version
```
---

## Inicialização de projeto
Após a instalação da dependência já é possível iniciar um projeto Django.
```powershell
# Comando para iniciar um projeto
django-admin startproject <nome_do_projeto>

# Comando para iniciar um projeto diretamente na raíz
django-admin startproject <nome_do_projeto> .
```

## Inicialização de aplicativo
Após iniciar o projeto, já é possível iniciar um aplicativo.  
Caso não esteja no diretório raíz do projeto, utilize o seguinte comando para navegar até ela:  
```powershell
# Comando para navegar até a pasta do projeto
cd <nome_do_projeto>

# Exemplo:
# Diretório inicial: projetos/
# Diretório final: projetos/nome_do_projeto
```

Assim que estiver no diretório do projeto, utilize o seguinte comando:
```powershell
python manage.py startapp <nome_do_app>
```
Uma estrutura como essa deve ter sido criada:  
```
nome_do_app/  
    ├── __init__.py 
    ├── admin.py  
    ├── apps.py  
    ├── migrations/  
    │   └── __init__.py  
    ├── models.py  
    ├── tests.py  
    └── views.py  
```