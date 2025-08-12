# Tutorial Passo a Passo: Site da Cafeteria StarCafé

Vamos criar um site simples para uma cafeteria inspirada no estilo da Starbucks. Este tutorial abrange desde a estrutura HTML básica até a estilização com CSS e interatividade com JavaScript.

## Mockup

![Mockup do site da Cafeteria StarCafé](mockup.png)
---

## 1. Estrutura Básica HTML

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Cafeteria Estilo Starbucks</title>
    <!-- Ícone da aba do navegador -->
    <link rel="icon" href="https://cdn1.iconfinder.com/data/icons/coffee-163/128/Hot_green_Coffee-512.png" type="image/png" />
</head>
<body>
    <!-- Conteúdo do site aqui -->
</body>
</html>
```

* O `<!DOCTYPE html>` indica que este é um documento HTML5.
* O `<html lang="pt-BR">` define que o conteúdo está em português do Brasil.
* `<meta charset="UTF-8" />` define a codificação de caracteres para suportar acentuação.
* `<meta name="viewport" ...>` garante que o site seja responsivo em dispositivos móveis.
* `<title>` define o título da aba no navegador.
* `<link rel="icon">` adiciona um ícone na aba.

---

## 2. Navegação (Navbar)

```html
<nav id="navbar">
    <div class="logo">StarCafé</div>
    <ul id="menu">
        <li><a href="#cafe-quente">Café Quente</a></li>
        <li><a href="#cafe-frio">Café Frio</a></li>
        <li><a href="#sobremesas">Sobremesas</a></li>
        <li><a href="#contato">Contato</a></li>
    </ul>
</nav>
```

* A `<nav>` cria a barra de navegação fixa no topo.
* `.logo` é o nome do site.
* A lista `<ul>` contém links para seções da página, facilitando a navegação interna.

---

## 3. Cabeçalho com Imagem e Título (Header)

```html
<header>
    <h1>StarCafé — Sabores que encantam</h1>
</header>
```

* O `<header>` tem uma imagem de fundo (definida no CSS) e o título principal do site.

---

## 7. Estilização (CSS)

### Reset e base

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: #f4f4f4;
    color: #333;
    line-height: 1.6;
}
```

* Remove margens e espaçamentos padrões.
* Define fonte e cores base.

---

### Navbar

```css
nav {
    position: fixed;
    top: 0;
    width: 100%;
    background: transparent;
    color: white;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 16px 32px;
    z-index: 1000;
    transition: background 0.3s ease, box-shadow 0.3s ease;
}

nav.scrolled {
    background: #006241;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
}

nav .logo {
    font-weight: bold;
    font-size: 24px;
    letter-spacing: 2px;
}

nav ul {
    list-style: none;
    display: flex;
    gap: 32px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: 600;
    transition: color 0.3s ease;
}

nav ul li a:hover {
    color: #a3d2ca;
}
```

* Navbar fixa no topo da página.
* Começa transparente e ganha cor e sombra ao rolar a página (classe `.scrolled`).
* Links com espaçamento e efeito de hover.

## Header

```css
/* Header */
header {
    background: url('https://images.unsplash.com/photo-1600093463592-8e36ae95ef56?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0') no-repeat center center/cover;
    height: 70vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.7);
    padding: 0 16px;
    padding-top: 60px;
    text-align: center;
}

header h1 {
    font-size: 48px;
    max-width: 700px;
    line-height: 1.2;
    animation: fadeInDown 1.5s ease forwards;
}
```