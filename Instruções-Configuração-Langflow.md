# Instruções de Configuração para Langflow

## 1. Criar Ambiente Virtual

### Windows:
```bash
python -m venv venv
```

### Mac/Linux:
```bash
python3 -m venv venv
```

## 2. Ativar o Ambiente Virtual

### Windows:
```bash
venv\Scripts\activate
```

### Mac/Linux:
```bash
source venv/bin/activate
```

## 3. Configurar Políticas de Execução no Windows

Abra o PowerShell como **Administrador** e execute os seguintes comandos:

```bash
Set-ExecutionPolicy unrestricted
Set-ExecutionPolicy RemoteSigned
```

## 4. Atualizar o Pip e Setup

### Windows e Mac/Linux:
```bash
python -m pip install --upgrade pip
python -m pip install --upgrade setuptools
```

## 5. Instalar Langflow

### Windows e Mac/Linux:
```bash
pip install langflow --upgrade
```

## 6. Executar o Langflow

### Windows e Mac/Linux:
```bash
python -m langflow run
```

## 7. Erro com DuckDB

Se você encontrar um erro relacionado ao **DuckDB**:

```bash
[notice] To update, run: python.exe -m pip install --upgrade pip
(venv) PS C:\projetos\langflow> python -m langflow run
2024-07-10 06:53:40.368 | ERROR    | langflow.services.factory:import_all_services_into_a_dict:81 - DLL load failed while importing duckdb: The specified module could not be found.
Traceback (most recent call last):
```

Este erro ocorre devido a bibliotecas ausentes do **C++**. Veja como corrigir.

### Windows:
Baixe a versão mais recente da DLL do Microsoft Visual C++:

[Link da DLL](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170#latest-microsoft-visual-c-redistributable-version)

**IMPORTANTE**: Baixe a versão **x64**.

## 8. Configurando Pasta de Componentes

Se precisar configurar o caminho para os componentes do Langflow, execute o seguinte comando:

### Windows:
```bash
setx LANGFLOW_COMPONENTS_PATH "C:\suapasta\pasta_langflow_components"
```

### Mac/Linux:
```bash
export LANGFLOW_COMPONENTS_PATH="/seu/caminho/pasta_langflow_components"
```
