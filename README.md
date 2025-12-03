
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Login - TechStore</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: rgba(0, 0, 0, 0.55); backdrop-filter: blur(4px);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #ffffff;
        }

        .login-container {
            background: rgba(68, 66, 66, 0.26);
            backdrop-filter: blur(10px);
            padding: 40px;
            width: 350px;
            border-radius: 20px;
            box-shadow: 0 0 20px rgba(225, 37, 231, 0.4);
            border: 1px solid rgba(104, 101, 241, 0.596);
            text-align: center;
        }

        .login-container h1 {
            margin-bottom: 20px;
            font-size: 26px;
            font-weight: 600;
            letter-spacing: 1px;
            color: #f7f8f8;
        }

        .input-group {
            text-align: left;
            margin-bottom: 20px;
        }

        .input-group label {
            font-size: 14px;
            display: block;
            margin-bottom: 6px;
            color: #f9f9fa;
        }

        .input-group input {
            width: 100%;
            padding: 10px;
            border-radius: 8px;
            border: none;
            outline: none;
            font-size: 15px;
            background: rgba(243, 223, 223, 0.295);
            color: rgb(241, 239, 239);
            border: 1px solid transparent;
            transition: 0.3s;
        }

        .input-group input:focus {
            border: 1px solid #f6f7f8;
        }

        .btn-login {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            background: #1a73e8;
            color: white;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn-login:hover {
            background: #0571dd;
        }

        .footer-text {
            margin-top: 18px;
            font-size: 13px;
            color: #0733b8;
        }

        .footer-text a {
            color: #4da6ff;
            text-decoration: none;
        }

        .footer-text a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body style="background: url('https://cdn.hobbyconsolas.com/sites/navi.axelspringer.es/public/media/image/2021/09/trust-gxt-1175-imperius-xl-2480661.jpg?tf=1200x') center/cover no-repeat; filter: blur(px);">
    <div style="
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 35px;
        background: rgba(146, 143, 143, 0.301);
        backdrop-filter: blur(6px);
        display: flex;
        justify-content: flex-end;
        align-items: center;
        padding-right: 25px;
        gap: 20px;
        font-family: 'Segoe UI', sans-serif;
    ">
        <a href="#" style="color: #086dd3; font-size: 14px; text-decoration:none;">Home</a>
        <a href="#" style="color: #0968c7; font-size: 14px; text-decoration:none;">Registrarte</a>
    </div>
    <div class="login-container">
        <h1>EasyPC</h1>

        <div class="input-group">
            <label for="usuario">Usuario:</label>
            <input type="text" id="usuario" placeholder="Ingresa tu usuario" />
        </div>

        <div class="input-group">
            <label for="password">Contraseña:</label>
            <input type="password" id="password" placeholder="Ingresa tu contraseña" />
        </div>

        <button class="btn-login">Iniciar Sesión</button>

        <p class="footer-text">¿No tienes cuenta? <a href="#">Regístrate aquí</a></p>
    </div>
    <script>
        const btn = document.querySelector('.btn-login');

        btn.addEventListener('click', () => {
            btn.innerHTML = 'Cargando... ';
            btn.style.background = '#264d73';
            btn.disabled = true;

            setTimeout(() => {
                // Palomita de listo
                btn.innerHTML = '✔ ';
                btn.style.background = '#28a745';

                // Pantalla de bienvenida
                setTimeout(() => {
                    document.body.innerHTML = `
                        <div style="
                            width: 100%;
                            height: 100vh;
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            flex-direction: column;
                            background: rgba(0, 0, 0, 0.55); backdrop-filter: blur(10px);
                            color: white;
                            text-align: center;
                            font-family: 'Segoe UI', sans-serif;
                        ">
                            <h1 style="font-size: 45px; margin-bottom: 20px; color:#4da6ff;">¡Bienvenido!</h1>
                            <p style="font-size: 18px; width: 60%; color:#b8c6ff;">Acceso concedido. Preparando tu experiencia en TechStore...</p>
                        </div>
                    `;
                }, 900);

            }, 2000);
        });
    </script>
</body>

