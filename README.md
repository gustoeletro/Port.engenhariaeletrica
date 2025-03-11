<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfólio de Engenharia Elétrica</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
            scroll-behavior: smooth;
        }
        body {
            background: #f4f4f4;
            color: #333;
        }
        header {
            background: #004080;
            color: white;
            padding: 20px;
            text-align: center;
            animation: fadeIn 1.5s ease-in;
        }
        nav {
            background: #002244;
            padding: 10px;
            text-align: center;
            position: sticky;
            top: 0;
            width: 100%;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-weight: bold;
            transition: 0.3s;
        }
        nav a:hover {
            color: #00aaff;
        }
        section {
            padding: 40px;
            text-align: center;
        }
        .container {
            max-width: 900px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.6s ease-in-out;
        }
        .show {
            opacity: 1;
            transform: translateY(0);
        }
        .projetos img {
            width: 100%;
            max-width: 300px;
            border-radius: 10px;
            margin: 10px;
            transition: transform 0.3s ease-in-out;
        }
        .projetos img:hover {
            transform: scale(1.1);
        }
        footer {
            background: #004080;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Media Query para Responsividade */
        @media (max-width: 768px) {
            nav a {
                display: block;
                margin: 10px 0;
            }

            .container {
                padding: 15px;
            }

            .projetos img {
                max-width: 100%;
                margin: 5px 0;
            }

            footer {
                font-size: 12px;
            }
        }

        /* Estilo para o Formulário de Contato */
        input, textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ddd;
        }

        button {
            background-color: #004080;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #00aaff;
        }
    </style>
</head>
<body>
    <header>
        <h1>Meu Portfólio de Engenharia Elétrica</h1>
    </header>
    
    <nav>
        <a href="#home">Home</a>
        <a href="#sobre">Sobre</a>
        <a href="#projetos">Projetos</a>
        <a href="#contato">Contato</a>
    </nav>
    
    <section id="home">
        <div class="container">
            <h2>Bem-vindo!</h2>
            <p>Este é o meu portfólio na área de Engenharia Elétrica, onde compartilho projetos, relatórios e estudos.</p>
        </div>
    </section>
    
    <section id="sobre">
        <div class="container">
            <h2>Sobre Mim</h2>
            <p>Sou um profissional em transição para a área de energia, estudando Engenharia Elétrica e buscando especialização.</p>
        </div>
    </section>
    
    <section id="projetos">
        <div class="container projetos">
            <h2>Projetos</h2>
            <p>Aqui estão algumas das minhas simulações e análises de circuitos elétricos.</p>
            <img src="https://via.placeholder.com/300x200/0000FF/808080?text=Circuito+1" alt="Projeto 1">
            <img src="https://via.placeholder.com/300x200/00FF00/808080?text=Circuito+2" alt="Projeto 2">
            <img src="https://via.placeholder.com/300x200/FF0000/808080?text=Circuito+3" alt="Projeto 3">
            <img src="https://via.placeholder.com/300x200/FFFF00/808080?text=Circuito+4" alt="Projeto 4">
        </div>
    </section>
    
    <section id="contato">
        <div class="container">
            <h2>Contato</h2>
            <form>
                <input type="text" placeholder="Seu nome" required><br><br>
                <input type="email" placeholder="Seu email" required><br><br>
                <textarea placeholder="Sua mensagem" rows="4" required></textarea><br><br>
                <button type="submit">Enviar</button>
            </form>
        </div>
    </section>
    
    <footer>
        <p>&copy; 2025 Meu Portfólio de Engenharia Elétrica</p>
    </footer>
    
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            const sections = document.querySelectorAll(".container");
            function reveal() {
                sections.forEach(section => {
                    const sectionTop = section.getBoundingClientRect().top;
                    if (sectionTop < window.innerHeight - 100) {
                        section.classList.add("show");
                    }
                });
            }
            window.addEventListener("scroll", reveal);
            reveal();
        });
    </script>
</body>
</html>
