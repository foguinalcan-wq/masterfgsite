<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MasterFG | Hub Oficial</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@700;900&family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --primary: #ff2a2a; 
            --primary-glow: rgba(255, 42, 42, 0.5);
            --bg-dark: #0d0d0d;
            --bg-card: #161616;
            --text: #ffffff;
            --download: #2ecc71;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Inter', sans-serif; }
        body { background-color: var(--bg-dark); color: var(--text); overflow-x: hidden; background-image: radial-gradient(circle at top center, #1a0505 0%, #0d0d0d 60%); }

        /* --- NAVEGAÇÃO --- */
        nav {
            display: flex; justify-content: space-between; align-items: center;
            padding: 15px 8%; background: rgba(0, 0, 0, 0.8); backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255, 42, 42, 0.3); position: sticky; top: 0; z-index: 1000;
        }
        .logo { font-weight: 900; font-size: 1.5rem; text-transform: uppercase; font-family: 'Poppins'; }
        .logo span { color: var(--primary); }
        .nav-links { display: flex; gap: 10px; align-items: center; }
        .nav-links a { color: #ccc; text-decoration: none; font-weight: 600; cursor: pointer; transition: 0.3s; font-size: 0.75rem; padding: 8px 12px; border-radius: 20px; }
        .nav-links a:hover, .nav-links a.active { color: #fff; background: var(--primary); }
        .btn-auth-nav { background: #222; border: 1px solid var(--primary); color: #fff !important; }

        /* --- PÁGINAS --- */
        .page { display: none; padding: 40px 8%; min-height: 85vh; animation: fadeIn 0.4s ease; }
        .page.active { display: block; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        /* --- AUTH FORM --- */
        .auth-container { max-width: 400px; margin: 40px auto; background: var(--bg-card); padding: 30px; border-radius: 20px; border: 1px solid #333; text-align: center; }
        .auth-input { width: 100%; padding: 12px; margin-bottom: 15px; background: #000; border: 1px solid #333; border-radius: 8px; color: #fff; outline: none; }
        .auth-input:focus { border-color: var(--primary); }
        .btn-main { width: 100%; padding: 12px; background: var(--primary); border: none; border-radius: 8px; color: #fff; font-weight: 800; cursor: pointer; transition: 0.3s; margin-top: 10px; }
        .btn-google { width: 100%; padding: 12px; background: #fff; color: #000; border: none; border-radius: 8px; font-weight: 700; cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 10px; margin-top: 15px; }
        .divider { margin: 20px 0; color: #555; font-size: 0.8rem; display: flex; align-items: center; gap: 10px; }
        .divider::before, .divider::after { content: ""; flex: 1; height: 1px; background: #333; }
        .toggle-auth { margin-top: 20px; font-size: 0.85rem; color: #aaa; }
        .toggle-auth span { color: var(--primary); cursor: pointer; font-weight: bold; }

        footer { text-align: center; padding: 40px; color: #444; font-size: 0.8rem; }
    </style>
</head>
<body>

    <nav>
        <div class="logo">MASTER<span>FG</span></div>
        <div class="nav-links">
            <a onclick="showPage('home')" id="link-home" class="active">INÍCIO</a>
            <a onclick="showPage('roms')" id="link-roms">ROMS</a>
            <a onclick="showPage('social')" id="link-social">REDES</a>
            <a onclick="showPage('login')" id="link-login" class="btn-auth-nav">ENTRAR</a>
        </div>
    </nav>

    <section id="home" class="page active">
        <div style="text-align: center;">
            <h1 style="font-size: 3rem; font-family: 'Poppins';">BEM-VINDO À TROPA</h1>
            <p id="user-welcome">Faça login para interagir com a comunidade!</p>
        </div>
    </section>

    <section id="login" class="page">
        <div class="auth-container">
            <h2 style="font-family: 'Poppins'; margin-bottom: 20px;">ENTRAR</h2>
            <input type="email" id="log-email" placeholder="Seu e-mail" class="auth-input">
            <input type="password" id="log-senha" placeholder="Sua senha" class="auth-input">
            <button class="btn-main" id="btn-login-manual">ENTRAR</button>
            <div class="divider">OU</div>
            <button class="btn-google" id="btn-login-google">
                <img src="https://upload.wikimedia.org/wikipedia/commons/5/53/Google_%22G%22_Logo.svg" width="18"> Entrar com Google
            </button>
            <p class="toggle-auth">Novo por aqui? <span onclick="showPage('register')">Criar conta</span></p>
        </div>
    </section>

    <section id="register" class="page">
        <div class="auth-container">
            <h2 style="font-family: 'Poppins'; margin-bottom: 20px;">CADASTRO</h2>
            <input type="text" id="reg-user" placeholder="Nome de usuário" class="auth-input">
            <input type="email" id="reg-email" placeholder="E-mail" class="auth-input">
            <input type="password" id="reg-senha" placeholder="Senha" class="auth-input">
            <button class="btn-main" id="btn-reg-manual">CRIAR MINHA CONTA</button>
            <div class="divider">OU</div>
            <button class="btn-google" id="btn-reg-google">
                <img src="https://upload.wikimedia.org/wikipedia/commons/5/53/Google_%22G%22_Logo.svg" width="18"> Cadastrar com Google
            </button>
            <p class="toggle-auth">Já tem conta? <span onclick="showPage('login')">Fazer Login</span></p>
        </div>
    </section>

    <footer>© 2026 MASTER FG</footer>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.7.1/firebase-app.js";
        import { getAuth, signInWithPopup, GoogleAuthProvider, createUserWithEmailAndPassword, signInWithEmailAndPassword, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/10.7.1/firebase-auth.js";

        const firebaseConfig = {
            apiKey: "AIzaSyDYj6KnmV2GTIqFX-Et4LPQHjuBAqn-SyA",
            authDomain: "site-masterfg.firebaseapp.com",
            projectId: "site-masterfg",
            storageBucket: "site-masterfg.firebasestorage.app",
            messagingSenderId: "523237984285",
            appId: "1:523237984285:web:fb6c39af58bdf3f1891ef4",
            measurementId: "G-52FLLL1Z0W"
        };

        const app = initializeApp(firebaseConfig);
        const auth = getAuth(app);
        const provider = new GoogleAuthProvider();

        // Login com Google
        const loginGoogle = async () => {
            try {
                await signInWithPopup(auth, provider);
                showPage('home');
            } catch (e) { alert("Erro Google: " + e.message); }
        };

        // Cadastro Manual
        const cadastroManual = async () => {
            const email = document.getElementById('reg-email').value;
            const senha = document.getElementById('reg-senha').value;
            try {
                await createUserWithEmailAndPassword(auth, email, senha);
                showPage('home');
            } catch (e) { alert("Erro Cadastro: " + e.message); }
        };

        // Login Manual
        const loginManual = async () => {
            const email = document.getElementById('log-email').value;
            const senha = document.getElementById('log-senha').value;
            try {
                await signInWithEmailAndPassword(auth, email, senha);
                showPage('home');
            } catch (e) { alert("E-mail ou senha inválidos."); }
        };

        // Observador de Estado (Verifica se está logado)
        onAuthStateChanged(auth, (user) => {
            if (user) {
                document.getElementById('user-welcome').innerText = "Salve, " + (user.displayName || user.email) + "! Você está logado.";
                document.getElementById('link-login').innerText = "SAIR";
                document.getElementById('link-login').onclick = () => auth.signOut();
            } else {
                document.getElementById('user-welcome').innerText = "Faça login para interagir com a comunidade!";
                document.getElementById('link-login').innerText = "ENTRAR";
                document.getElementById('link-login').onclick = () => showPage('login');
            }
        });

        // Atribuir eventos aos botões
        document.getElementById('btn-login-google').onclick = loginGoogle;
        document.getElementById('btn-reg-google').onclick = loginGoogle;
        document.getElementById('btn-reg-manual').onclick = cadastroManual;
        document.getElementById('btn-login-manual').onclick = loginManual;

    </script>

    <script>
        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
            document.querySelectorAll('.nav-links a').forEach(l => l.classList.remove('active'));
            document.getElementById(pageId).classList.add('active');
            const navId = (pageId === 'register') ? 'link-login' : 'link-' + pageId;
            if(document.getElementById(navId)) document.getElementById(navId).classList.add('active');
            window.scrollTo(0,0);
        }
    </script>
</body>
</html>
