
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Repositorio GitHub - Monografía Holográfica</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #ecf0f1;
            min-height: 100vh;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            display: grid;
            grid-template-columns: 1fr;
            gap: 30px;
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            background: rgba(25, 35, 45, 0.8);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(52, 152, 219, 0.3);
            margin-bottom: 20px;
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 15px;
            color: #fff;
            text-shadow: 0 0 15px rgba(52, 152, 219, 0.6);
        }
        
        .subtitle {
            font-size: 1.4rem;
            max-width: 800px;
            margin: 0 auto 30px;
            color: #bdc3c7;
        }
        
        .github-card {
            background: rgba(25, 35, 45, 0.8);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(46, 204, 113, 0.3);
            text-align: center;
        }
        
        .github-icon {
            font-size: 5rem;
            color: #6cc644;
            margin-bottom: 20px;
            text-shadow: 0 0 20px rgba(108, 198, 68, 0.5);
        }
        
        .repo-title {
            font-size: 2.2rem;
            margin-bottom: 15px;
            color: #fff;
        }
        
        .repo-desc {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
            color: #bdc3c7;
        }
        
        .repo-link {
            display: inline-block;
            background: #24292e;
            color: white;
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-size: 1.3rem;
            font-weight: 600;
            transition: all 0.3s ease;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            border: 1px solid #6cc644;
        }
        
        .repo-link:hover {
            transform: translateY(-5px);
            background: #2d3339;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
        }
        
        .repo-link i {
            margin-right: 10px;
        }
        
        .repo-stats {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }
        
        .stat-item {
            background: rgba(36, 41, 46, 0.6);
            padding: 20px 30px;
            border-radius: 15px;
            min-width: 180px;
            border: 1px solid rgba(108, 198, 68, 0.3);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #6cc644;
            margin-bottom: 5px;
        }
        
        .stat-label {
            font-size: 1.1rem;
            color: #bdc3c7;
        }
        
        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }
        
        .content-card {
            background: rgba(36, 41, 46, 0.6);
            border-radius: 15px;
            padding: 25px;
            border-left: 4px solid #6cc644;
            transition: transform 0.3s ease;
        }
        
        .content-card:hover {
            transform: translateY(-10px);
        }
        
        .card-title {
            font-size: 1.5rem;
            color: #fff;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .card-icon {
            color: #6cc644;
            font-size: 1.8rem;
        }
        
        .card-list {
            list-style-type: none;
        }
        
        .card-list li {
            padding: 10px 0;
            border-bottom: 1px solid rgba(108, 198, 68, 0.2);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .card-list li:last-child {
            border-bottom: none;
        }
        
        .card-list i {
            color: #6cc644;
            min-width: 25px;
        }
        
        .download-section {
            background: rgba(25, 35, 45, 0.8);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(231, 76, 60, 0.3);
            text-align: center;
        }
        
        .download-title {
            font-size: 2rem;
            margin-bottom: 30px;
            color: #fff;
        }
        
        .download-options {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .download-btn {
            display: flex;
            flex-direction: column;
            align-items: center;
            background: rgba(44, 62, 80, 0.6);
            border-radius: 15px;
            padding: 25px;
            min-width: 200px;
            text-decoration: none;
            color: #ecf0f1;
            transition: all 0.3s ease;
            border: 1px solid rgba(52, 152, 219, 0.3);
        }
        
        .download-btn:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            border-color: #3498db;
        }
        
        .download-icon {
            font-size: 3rem;
            margin-bottom: 15px;
            color: #3498db;
        }
        
        .btn-text {
            font-size: 1.1rem;
            font-weight: 600;
        }
        
        .btn-subtext {
            font-size: 0.9rem;
            color: #bdc3c7;
            margin-top: 5px;
        }
        
        footer {
            text-align: center;
            padding: 40px 20px;
            margin-top: 50px;
            color: #bdc3c7;
            font-size: 1rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .contact {
            margin-top: 20px;
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            color: #3498db;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            
            .subtitle {
                font-size: 1.2rem;
            }
            
            .repo-title {
                font-size: 1.8rem;
            }
            
            .stat-item {
                min-width: 140px;
                padding: 15px 20px;
            }
            
            .stat-number {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1><i class="fab fa-github"></i> Repositorio GitHub</h1>
            <p class="subtitle">Monografía completa: "El Principio Holográfico en Sistemas Naturales"</p>
        </header>
        
        <section class="github-card">
            <i class="fab fa-github github-icon"></i>
            <h2 class="repo-title">jteran-ai/holografia-natural</h2>
            <p class="repo-desc">Repositorio oficial con todos los recursos, scripts, datos y documentos de la investigación doctoral sobre el principio holográfico en sistemas naturales.</p>
            
            <a href="https://github.com/jteran-ai/holografia-natural" class="repo-link" target="_blank">
                <i class="fab fa-github"></i> Acceder al Repositorio
            </a>
            
            <div class="repo-stats">
                <div class="stat-item">
                    <div class="stat-number">220</div>
                    <div class="stat-label">Páginas</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">43</div>
                    <div class="stat-label">Figuras</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">18</div>
                    <div class="stat-label">Tablas</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">12</div>
                    <div class="stat-label">Scripts</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">178</div>
                    <div class="stat-label">Referencias</div>
                </div>
            </div>
            
            <h3 style="color: #fff; margin-bottom: 20px; font-size: 1.8rem;">Contenido del Repositorio</h3>
            
            <div class="content-grid">
                <div class="content-card">
                    <h4 class="card-title"><i class="fas fa-file-alt card-icon"></i> Documentos</h4>
                    <ul class="card-list">
                        <li><i class="fas fa-check-circle"></i> Monografía completa (PDF)</li>
                        <li><i class="fas fa-check-circle"></i> Presentaciones académicas</li>
                        <li><i class="fas fa-check-circle"></i> Artículos relacionados</li>
                        <li><i class="fas fa-check-circle"></i> Resúmenes ejecutivos</li>
                        <li><i class="fas fa-check-circle"></i> Propuestas de investigación</li>
                    </ul>
                </div>
                
                <div class="content-card">
                    <h4 class="card-title"><i class="fas fa-code card-icon"></i> Código</h4>
                    <ul class="card-list">
                        <li><i class="fab fa-python"></i> Scripts Python (FDTD, QuTiP)</li>
                        <li><i class="fas fa-project-diagram"></i> Simulaciones computacionales</li>
                        <li><i class="fas fa-brain"></i> Modelos neuronales</li>
                        <li><i class="fas fa-calculator"></i> Análisis de datos</li>
                        <li><i class="fas fa-chart-bar"></i> Visualizaciones científicas</li>
                    </ul>
                </div>
                
                <div class="content-card">
                    <h4 class="card-title"><i class="fas fa-database card-icon"></i> Datos</h4>
                    <ul class="card-list">
                        <li><i class="fas fa-microscope"></i> Resultados experimentales</li>
                        <li><i class="fas fa-cloud"></i> Datos cosmológicos (CMB)</li>
                        <li><i class="fas fa-brain"></i> fMRI y datos neuronales</li>
                        <li><i class="fas fa-atom"></i> Simulaciones cuánticas</li>
                        <li><i class="fas fa-file-csv"></i> Conjuntos de datos estructurados</li>
                    </ul>
                </div>
            </div>
        </section>
        
        <section class="download-section">
            <h2 class="download-title">Descargas Directas</h2>
            <div class="download-options">
                <a href="#" class="download-btn">
                    <i class="fas fa-file-pdf download-icon"></i>
                    <span class="btn-text">Monografía Completa</span>
                    <span class="btn-subtext">PDF · 220 páginas</span>
                </a>
                
                <a href="#" class="download-btn">
                    <i class="fas fa-file-code download-icon"></i>
                    <span class="btn-text">Scripts Python</span>
                    <span class="btn-subtext">ZIP · 12 archivos</span>
                </a>
                
                <a href="#" class="download-btn">
                    <i class="fas fa-database download-icon"></i>
                    <span class="btn-text">Datos de Investigación</span>
                    <span class="btn-subtext">CSV · 15 datasets</span>
                </a>
                
                <a href="#" class="download-btn">
                    <i class="fas fa-book download-icon"></i>
                    <span class="btn-text">Bibliografía Completa</span>
                    <span class="btn-subtext">BibTeX · 178 referencias</span>
                </a>
            </div>
        </section>
        
        <footer>
            <p>© 2023 Dr. JTeran-AI | Departamento de Física Teórica y del Cosmos</p>
            <p>Licencia Creative Commons Atribución-NoComercial 4.0 Internacional</p>
            
            <div class="contact">
                <div class="contact-item">
                    <i class="fab fa-github"></i>
                    <span>github.com/jteran-ai</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>jteran@universidad.edu</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-book"></i>
                    <span>DOI: 10.1000/xyz123</span>
                </div>
            </div>
        </footer>
    </div>
    
    <script>
        // Simulación de descargas
        const downloadButtons = document.querySelectorAll('.download-btn');
        
        downloadButtons.forEach(button => {
            button.addEventListener('click', function(e) {
                e.preventDefault();
                
                // Determinar tipo de descarga
                let downloadType = "archivo";
                if(this.querySelector('.fa-file-pdf')) downloadType = "monografía";
                if(this.querySelector('.fa-file-code')) downloadType = "scripts";
                if(this.querySelector('.fa-database')) downloadType = "datos";
                if(this.querySelector('.fa-book')) downloadType = "bibliografía";
                
                // Crear mensaje de descarga
                const downloadMessage = document.createElement('div');
                downloadMessage.innerHTML = `
                    <div style="position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.9); z-index: 1000; display: flex; justify-content: center; align-items: center;">
                        <div style="background: #2c3e50; padding: 40px; border-radius: 20px; text-align: center; max-width: 500px; border: 2px solid #3498db;">
                            <h2 style="color: #3498db; margin-bottom: 20px;"><i class="fas fa-download"></i> Descarga Iniciada</h2>
                            <p style="margin-bottom: 30px; font-size: 1.1rem;">Su ${downloadType} se está descargando. Por favor, no cierre esta ventana.</p>
                            <div style="width: 100%; height: 20px; background: #1a1a1a; border-radius: 10px; margin-bottom: 30px; overflow: hidden;">
                                <div id="progressBar" style="height: 100%; background: linear-gradient(90deg, #3498db, #2ecc71); width: 0%; transition: width 2s;"></div>
                            </div>
                            <p id="progressText" style="margin-bottom: 30px;">Preparando descarga... 0%</p>
                            <button id="closeBtn" style="display: none; background: #3498db; color: white; border: none; padding: 12px 30px; border-radius: 8px; cursor: pointer; font-size: 1rem; font-weight: 600;">Cerrar</button>
                        </div>
                    </div>
                `;
                
                document.body.appendChild(downloadMessage);
                
                // Simular progreso de descarga
                let progress = 0;
                const progressBar = document.getElementById('progressBar');
                const progressText = document.getElementById('progressText');
                const closeBtn = document.getElementById('closeBtn');
                
                const interval = setInterval(() => {
                    progress += 5;
                    progressBar.style.width = progress + '%';
                    progressText.textContent = `Descargando... ${progress}% completado`;
                    
                    if (progress >= 100) {
                        clearInterval(interval);
                        progressText.innerHTML = '<span style="color:#2ecc71"><i class="fas fa-check-circle"></i> ¡Descarga completada con éxito!</span>';
                        closeBtn.style.display = 'block';
                        
                        closeBtn.addEventListener('click', function() {
                            document.body.removeChild(downloadMessage);
                        });
                    }
                }, 200);
            });
        });
    </script>
</body>
</html>