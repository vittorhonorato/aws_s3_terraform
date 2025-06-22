# Terraform AWS S3 Bucket

Projeto de infraestrutura como código utilizando [Terraform](https://www.terraform.io/) para provisionamento de um bucket S3 na AWS. Inclui automação de deploy via GitHub Actions.

---

## 📁 Estrutura do Projeto
```
infra/
  s3-bucket/
    main.tf
    bucket.tf
.github/
  workflows/
    terraform.yml
```
- `infra/s3-bucket/main.tf`: Configuração do provider AWS e requisitos do Terraform.
- `infra/s3-bucket/bucket.tf`: Definição do recurso S3 Bucket.
- `.github/workflows/terraform.yml`: Pipeline de CI/CD para validação e aplicação automática do Terraform via GitHub Actions.


---

## ✅ Pré-requisitos

- Conta AWS com permissões para gerenciamento de S3.
- [Terraform >= 1.3.0](https://www.terraform.io/downloads.html) instalado.
- Repositório GitHub com os **Secrets** configurados:
  - `AWS_ACCESS_KEY_ID`
  - `AWS_SECRET_ACCESS_KEY`

---

## 🚀 Como Usar

### 🔧 1. Clonar o repositório

```bash
git clone https://github.com/vittorhonorato/aws_s3_terraform.git
cd aws_s3_terraform/infra/s3-bucket
```

### 🧪 2. Executar localmente

```bash
terraform init
terraform validate
terraform plan
terraform apply
```
Dica: use terraform destroy para remover os recursos provisionados.

### 🤖 3. Automatizar com CI/CD
1. 🔧 Acesse as configurações do repositório no GitHub.

2. 🔐 Vá até **Secrets and variables > Actions** e adicione:

- 🔑 `AWS_ACCESS_KEY_ID`
- 🔒 `AWS_SECRET_ACCESS_KEY`

3. 🚀 Faça push para a branch `main` e o workflow será acionado automaticamente.

---
## ⚙️ CI/CD com GitHub Actions

O workflow localizado em `.github/workflows/terraform.yml` executa automaticamente os seguintes passos a cada push na branch `main`:

- 🧱 `terraform init`
- ✅ `terraform validate`
- 📊 `terraform plan`
- 🚀 `terraform apply` (com aprovação, se necessário)

---

## 📚 Objetivo

Projeto desenvolvido com fins educacionais para estudo de:

- 🛠️ Provisionamento com Terraform  
- 🤖 Automação com GitHub Actions  
- ☁️ Práticas de DevOps em nuvem (AWS)







