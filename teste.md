# 📘 Aula Completa de CSS: Do Inline ao Externo (com Classes e IDs)

## 🔍 Objetivo da Aula

Ensinar os alunos a migrar do uso de **CSS inline** para **CSS interno** e **CSS externo**, apresentando também o uso correto de **classes (`.classe`)** e **IDs (`#id`)**, boas práticas e exemplos práticos.

**Duração:** 90 minutos
**Nível:** Intermediário

---

## ⚙️ Parte 1: Introdução ao CSS Inline (10 min)

### Exemplo:

```html
<h1 style="color: blue; font-size: 24px;">Bem-vindo!</h1>
<p style="color: gray;">Este é um exemplo de CSS inline.</p>
```

### Pontos para Discussão:

* ⚠️ Dificuldade de manutenção (precisa mudar em cada elemento)
* ⚠️ Código poluído e repetitivo
* ✅ Ideal apenas para **testes rápidos** ou **ajustes pontuais**

**Conclusão:** Precisamos separar o estilo da estrutura do HTML.

---

## 🖋️ Parte 2: CSS Interno (<style>) (25 min)

### Exemplo:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Exemplo CSS Interno</title>
  <style>
    h1 {
      color: darkblue;
      text-align: center;
    }

    p {
      color: gray;
      font-size: 16px;
    }
  </style>
</head>
<body>
  <h1>Minha Página</h1>
  <p>Agora os estilos estão dentro da tag &lt;style&gt;!</p>
</body>
</html>
```

### Atividade:

1. Reproduzir o exemplo.
2. Alterar o **background** e as **margens**.

**Conclusão:** O CSS ficou centralizado, mas ainda dentro do HTML.

---

## 👀 Parte 3: Classes e IDs (15 min)

### Diferenças

| Tipo       | Símbolo | Função                             | Pode repetir? |
| ---------- | ------- | ---------------------------------- | ------------- |
| **Classe** | `.`     | Agrupar vários elementos parecidos | ✅ Sim         |
| **ID**     | `#`     | Identificar um elemento único      | ❌ Não         |

### Exemplo de Classe:

```html
<style>
  .botao {
    background-color: #007BFF;
    color: white;
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
  }
  .botao:hover {
    background-color: #0056b3;
  }
</style>

<button class="botao">Salvar</button>
<button class="botao">Cancelar</button>
```

💡 **Use classe quando quiser repetir o estilo em vários elementos.**

### Exemplo de ID:

```html
<style>
  #cabecalho {
    background-color: darkgreen;
    color: white;
    text-align: center;
    padding: 20px;
  }
</style>

<header id="cabecalho">
  <h1>Meu Site</h1>
</header>
```

🔊 **Use ID quando o estilo se aplica a um único elemento.**

### Combinação de Ambos:

```html
<style>
  .secao {
    padding: 20px;
    border: 1px solid #ccc;
  }
  #sobre {
    background-color: #f0f8ff;
  }
  #contato {
    background-color: #fff0f0;
  }
</style>

<section id="sobre" class="secao">Sobre Nós</section>
<section id="contato" class="secao">Contato</section>
```

🔄 **Melhor prática:** use `class` para o estilo geral e `id` para identificar seções únicas.

---

## 📁 Parte 4: CSS Externo (25 min)

### Estrutura de Arquivos:

```
index.html
style.css
```

#### index.html

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Meu Site com CSS Externo</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header id="topo">
    <h1>Minha Página com CSS Externo</h1>
    <p class="subtitulo">Aprendendo a separar o CSS</p>
  </header>

  <section>
    <p>Agora os estilos vêm de um arquivo separado!</p>
    <button class="btn">Clique Aqui</button>
  </section>

  <footer id="rodape">
    <p>&copy; 2025 - Meu Site</p>
  </footer>
</body>
</html>
```

#### style.css

```css
body {
  font-family: Arial, sans-serif;
  background-color: #f8f9fa;
  margin: 0;
  padding: 20px;
}

#topo {
  background-color: #007BFF;
  color: white;
  text-align: center;
  padding: 15px;
}

.subtitulo {
  font-size: 18px;
  color: #f1f1f1;
}

.btn {
  background-color: #007BFF;
  color: white;
  border: none;
  padding: 10px 15px;
  border-radius: 5px;
  cursor: pointer;
}
.btn:hover {
  background-color: #0056b3;
}

#rodape {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px;
  margin-top: 30px;
}
```

**Discussão:**

* CSS externo é o mais **profissional**.
* Facilita a **manutenção** e o **reuso** entre várias páginas.

---

## 🔍 Revisão Final

| Conceito    | Função                    | Exemplo                       |
| ----------- | ------------------------- | ----------------------------- |
| **Inline**  | Estilo direto no elemento | `<p style="color:red">`       |
| **Interno** | Dentro da tag `<style>`   | `<style>p{color:red}</style>` |
| **Externo** | Em arquivo separado       | `style.css` + `<link>`        |
| **Classe**  | Reutilizável              | `.botao { ... }`              |
| **ID**      | Único                     | `#rodape { ... }`             |

---

**Mensagem final:**

> "HTML cria o corpo. CSS cria o estilo. Juntos, dão vida à sua página!"
