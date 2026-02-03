# 📚 Exercício Spring 2 – Modelo de Domínio e ORM

Projeto desenvolvido como parte da formação **Desenvolvedor Moderno (Back end – Spring Boot)**, no capítulo **Modelo de domínio e ORM**.

O objetivo é implementar um **sistema de eventos acadêmicos** utilizando **Spring Boot**, **JPA/Hibernate** e **H2 Database**, com mapeamento de entidades e relacionamentos conforme o diagrama conceitual proposto.

---

## 🚀 Tecnologias Utilizadas

- ☕ **Java 25**
- 🌱 **Spring Boot 4.0.2**
- 🗄 **Spring Data JPA / Hibernate**
- 🧪 **H2 Database**
- 📦 **Maven**

---

## 📖 Descrição do Sistema

O sistema gerencia informações relacionadas a um **evento acadêmico**, incluindo:

- Atividades do evento
- Blocos de horários das atividades
- Categorias
- Participantes inscritos

---

## 🧩 Entidades do Sistema

### 👤 Participante
- `id`
- `nome`
- `email`

**Relacionamento:**
- Many-to-Many com **Atividade**

---

### 📘 Atividade
- `id`
- `nome`
- `descrição`
- `preço`

**Relacionamentos:**
- Many-to-One com **Categoria**
- One-to-Many com **Bloco**
- Many-to-Many com **Participante**

---

### 🏷 Categoria
- `id`
- `descrição`

**Relacionamento:**
- One-to-Many com **Atividade**

---

### ⏱ Bloco
- `id`
- `início`
- `fim`

**Relacionamento:**
- Many-to-One com **Atividade**

---

## 🗄️ Estrutura do Banco de Dados

O banco de dados é inicializado automaticamente via **`data.sql`** durante a inicialização da aplicação.

### 📊 Exemplos de Dados Inseridos

- **Participantes:**  
  José Silva, Tiago Faria, Maria do Rosario, Teresa Silva

- **Categorias:**  
  Curso, Oficina

- **Atividades:**  
  Curso de HTML, Oficina de GitHub

- **Blocos:**  
  Horários associados às atividades

- **Relações:**  
  Participantes vinculados às atividades (Many-to-Many)

---

## ▶️ Como Executar o Projeto

### 1️⃣ Clone o repositório

```bash
git clone https://github.com/giuliano6943/exercicio-spring2.git
```
---
👨‍💻 Autor

Projeto desenvolvido por Giuliano como parte da formação Java Spring Professional.
