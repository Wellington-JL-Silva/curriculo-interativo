
<!DOCTYPE html>
<html lang="pt-br">
<head>
// Por: Wellington Silva - www.linkedin.com/in/wellingtonsilva-1997-
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Template de Currículo Profissional Editável</title>

    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    
    <style>
        body {
            font-family: 'Inter', sans-serif;
            -webkit-print-color-adjust: exact;
        }
        :root {
            --primary-color: #2c5282;
            --secondary-color: #2d3748;
        }
        .section-title {
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 8px;
            margin-bottom: 16px;
            font-weight: 600;
            color: var(--secondary-color);
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        #profilePhoto.interactive:hover {
            cursor: pointer;
            opacity: 0.8;
        }
        [contenteditable="true"] {
            outline: 2px dashed #f9d6d3;
            padding: 2px 4px;
            border-radius: 4px;
            cursor: text;
            transition: background-color 0.3s;
        }
        [contenteditable="true"]:hover, [contenteditable="true"]:focus {
            background-color: #fff8f7;
            outline-color: #c0392b;
        }
        .instruction-text {
            color: #999;
            font-style: italic;
            font-size: 0.9em;
        }
        @media print {
            body { margin: 0; padding: 0; font-size: 10pt; }
            .no-print { display: none; }
            #curriculumContent { margin: 0 !important; box-shadow: none !important; border: none !important; }
            aside, main { padding: 1.25rem; }
            [contenteditable="true"] { outline: none; padding: 2px 4px; }
        }
    </style>
</head>
<body class="bg-gray-100">

    <div id="curriculumContent" class="max-w-4xl mx-auto my-10 bg-white shadow-lg print:shadow-none">
        <div class="flex flex-col md:flex-row">
            
            <aside class="w-full md:w-1/2 bg-gray-50 text-gray-800 p-8 print:bg-gray-50">
                <div class="flex flex-col items-center">
                    <img src="https://via.placeholder.com/150" alt="Sua Foto Profissional" id="profilePhoto" class="rounded-full w-36 h-36 mb-4 border-4 border-[var(--primary-color)] object-cover interactive">
                    <input type="file" id="photoUpload" class="hidden" accept="image/*">
                    <h1 class="text-2xl font-bold text-center text-[var(--secondary-color)]" contenteditable="true">[Seu Nome Completo]</h1>
                    <h2 class="text-md text-center text-[var(--primary-color)] font-semibold" contenteditable="true">[Seu Cargo ou Título Profissional]</h2>
                </div>

                <div class="mt-4">
                    <h2 class="text-lg font-semibold border-b-2 border-[var(--primary-color)] pb-2 mb-3 text-[var(--secondary-color)]">CONTATO</h2>
                    <ul class="space-y-2 text-sm">
                        <li class="flex items-start"><i class="fas fa-map-marker-alt w-5 mr-3 text-[var(--primary-color)] pt-1"></i><span contenteditable="true">[Sua Cidade, Estado]</span></li>
                        <li class="flex items-start"><i class="fas fa-rocket w-5 mr-3 text-[var(--primary-color)] pt-1"></i><span contenteditable="true">[Sua disponibilidade. Ex: Disponibilidade para viagens]</span></li>
                        <li class="flex items-center"><i class="fas fa-phone w-5 mr-3 text-[var(--primary-color)]"></i><span contenteditable="true">[(XX) XXXXX-XXXX]</span></li>
                        <li class="flex items-center"><i class="fas fa-envelope w-5 mr-3 text-[var(--primary-color)]"></i><a href="mailto:seu.email@exemplo.com" class="hover:text-blue-800 break-all" contenteditable="true">[seu.email@exemplo.com]</a></li>
                    </ul>
                </div>

                <div class="mt-4">
                    <h2 class="text-lg font-semibold border-b-2 border-[var(--primary-color)] pb-2 mb-3 text-[var(--secondary-color)]">COMPETÊNCIAS</h2>
                    <div contenteditable="true">
                        <ul class="space-y-3 text-sm">
                            <li><span class="font-semibold">[Competência Chave 1]:</span> [Descreva-a. Ex: Análise de Dados para tomada de decisão estratégica.]</li>
                            <li><span class="font-semibold">[Competência Chave 2]:</span> [Descreva-a. Ex: Liderança de equipes e desenvolvimento de talentos.]</li>
                            <li><span class="font-semibold">[Competência Chave 3]:</span> [Descreva-a. Ex: Gestão de Projetos com foco em metodologias ágeis.]</li>
                            <li><span class="font-semibold">[Competência Chave 4]:</span> [Descreva-a. Ex: Fluência em softwares específicos como SAP, Power BI, etc.]</li>
                        </ul>
                    </div>
                </div>

                <div class="mt-4">
                    <h2 class="text-lg font-semibold border-b-2 border-[var(--primary-color)] pb-2 mb-3 text-[var(--secondary-color)]">FORMAÇÃO</h2>
                     <div contenteditable="true">
                        <div class="space-y-2">
                            <div>
                                <h3 class="font-bold text-sm">[Nome da sua Graduação ou Formação Principal]</h3>
                                <p class="text-xs text-gray-700">[Nome da Instituição] | [Status: Cursando ou Ano de Conclusão]</p>
                            </div>
                            <p class="text-sm"><span class="font-bold">[Nome do Curso Técnico ou Secundário]</span> <span class="text-gray-700 text-xs">| [Instituição] - [Ano de Conclusão]</span></p>
                        </div>
                    </div>
                </div>

                 <div class="mt-4">
                    <h2 class="text-lg font-semibold border-b-2 border-[var(--primary-color)] pb-2 mb-3 text-[var(--secondary-color)]">CERTIFICAÇÕES & CURSOS</h2>
                      <div contenteditable="true">
                        <div class="space-y-2">
                            <p class="text-sm"><span class="font-bold">[Nome da Certificação]</span> <span class="text-gray-700 text-xs">| [Instituição Emissora]</span></p>
                            <p class="text-sm"><span class="font-bold">[Nome do Curso Relevante]</span> <span class="text-gray-700 text-xs">| [Instituição]</span></p>
                        </div>
                    </div>
                </div>
            </aside>

            <main class="w-full md:w-1/2 p-8">
                <section>
                    <h2 class="text-2xl font-bold text-[var(--primary-color)] mb-2">OBJETIVO</h2>
                    <p class="text-gray-800 leading-relaxed text-sm" contenteditable="true">
                       [Escreva aqui seu objetivo profissional em 2-3 linhas. Destaque sua principal proposta de valor. Ex: Profissional de Marketing com 5 anos de experiência em estratégias digitais, buscando uma posição para liderar campanhas de crescimento e otimizar a performance de canais de aquisição.]
                    </p>
                </section>

                <section class="mt-6">
                    <h2 class="section-title text-xl">EXPERIÊNCIA PROFISSIONAL</h2>
                    <p class="instruction-text">(Liste da mais recente para a mais antiga)</p>
                    <div class="space-y-4" contenteditable="true">
                        <div class="relative pl-4">
                              <div class="absolute top-1 left-0 h-full w-0.5 bg-gray-200"></div>
                              <div class="absolute top-1 left-[-4px] w-3 h-3 bg-[var(--primary-color)] rounded-full"></div>
                            <p class="text-xs text-gray-600">[Mês/Ano de Início] - Atualmente</p>
                            <h3 class="font-bold text-[var(--secondary-color)]">[Seu Cargo Atual]</h3>
                            <p class="text-sm font-semibold text-gray-700">[Nome da Empresa Atual]</p>
                            <ul class="list-disc list-inside text-sm mt-1 space-y-1 text-gray-800">
                                <li>[Descreva sua principal conquista. Use verbos de ação e números. Ex: "Liderei a reestruturação do processo de vendas, resultando em um aumento de 15% no faturamento."].</li>
                                <li>[Outra conquista ou responsabilidade relevante.].</li>
                            </ul>
                        </div>
                        <div class="relative pl-4">
                              <div class="absolute top-1 left-0 h-full w-0.5 bg-gray-200"></div>
                              <div class="absolute top-1 left-[-4px] w-3 h-3 bg-[var(--primary-color)] rounded-full"></div>
                            <p class="text-xs text-gray-600">[Mês/Ano de Início] - [Mês/Ano de Fim]</p>
                            <h3 class="font-bold text-[var(--secondary-color)]">[Seu Cargo Anterior]</h3>
                            <p class="text-sm font-semibold text-gray-700">[Nome da Empresa Anterior]</p>
                            <ul class="list-disc list-inside text-sm mt-1 space-y-1 text-gray-800">
                                <li>[Conquista ou responsabilidade 1. Ex: "Desenvolvi e executei 10+ campanhas de marketing digital, alcançando mais de 2 milhões de usuários."].</li>
                                <li>[Conquista ou responsabilidade 2.].</li>
                            </ul>
                        </div>
                    </div>
                </section>
            </main>
        </div>
    </div>

    <div class="text-center py-5 no-print space-x-2 md:space-x-4">
        <button id="downloadPngButton" class="bg-[var(--primary-color)] hover:opacity-90 text-white font-bold py-2 px-4 rounded-lg shadow-md transition-opacity">
            <i class="fas fa-image mr-2"></i><span class="hidden md:inline">Baixar Imagem (PNG)</span>
        </button>
        <button id="downloadHtmlButton" class="bg-[var(--secondary-color)] hover:opacity-90 text-white font-bold py-2 px-4 rounded-lg shadow-md transition-opacity">
            <i class="fas fa-code mr-2"></i><span class="hidden md:inline">Baixar HTML</span>
        </button>
        <button id="downloadPdfButton" class="bg-red-700 hover:bg-red-800 text-white font-bold py-2 px-4 rounded-lg shadow-md transition-colors">
            <i class="fas fa-file-pdf mr-2"></i><span class="hidden md:inline">Baixar PDF</span>
        </button>
    </div>

    <script>
        // Por: Wellington Silva - www.linkedin.com/in/wellingtonsilva-1997-
        // Pensamento: É uma boa prática declarar todas as constantes que manipulam o DOM no início do script.
        // Mapeia os elementos do HTML para variáveis no JavaScript.
        const { jsPDF } = window.jspdf;
        const profilePhoto = document.getElementById('profilePhoto');
        const photoUpload = document.getElementById('photoUpload');
        const downloadPngButton = document.getElementById('downloadPngButton');
        const downloadHtmlButton = document.getElementById('downloadHtmlButton');
        const downloadPdfButton = document.getElementById('downloadPdfButton');

        // Por: Wellington Silva - www.linkedin.com/in/wellingtonsilva-1997-
        // Pensamento: O upload de foto precisa ser iniciado por um clique no elemento da imagem, não em um botão de arquivo visível.
        // Adiciona um "ouvinte" que simula o clique no input de arquivo quando a foto é clicada.
        profilePhoto.addEventListener('click', () => photoUpload.click());

        // Por: Wellington Silva - www.linkedin.com/in/wellingtonsilva-1997-
        // Pensamento: Após o usuário escolher um arquivo, preciso lê-lo e exibi-lo na página.
        // Função que lê o arquivo de imagem selecionado e o exibe no lugar da foto de placeholder.
        photoUpload.addEventListener('change', (event) => {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = (e) => { profilePhoto.src = e.target.result; }
                reader.readAsDataURL(file);
            }
        });

        // Por: Wellington Silva - www.linkedin.com/in/wellingtonsilva-1997-
        // Pensamento: A função de download precisa ser reutilizável para PNG e PDF, e deve fornecer feedback visual ao usuário.
        // Função principal que lida com os downloads (PNG e PDF).
        const handleDownload = (button, format) => {
            const element = document.getElementById('curriculumContent');
            const originalButtonText = button.innerHTML;

            button.innerHTML = `<i class="fas fa-spinner fa-spin mr-2"></i>Gerando...`;
            button.disabled = true;
            
            const editableFields = document.querySelectorAll('[contenteditable="true"]');
            editableFields.forEach(field => field.style.outline = 'none');

            html2canvas(element, { 
                scale: 2,
                useCORS: true, 
                logging: false, 
                letterRendering: true 
            })
                .then(canvas => {
                    const fileName = 'Meu_Curriculo_Profissional';
                    if (format === 'png') {
                        const link = document.createElement('a');
                        link.download = `${fileName}.png`;
                        link.href = canvas.toDataURL('image/png');
                        link.click();
                    } 
                    else if (format === 'pdf') {
                        const imgData = canvas.toDataURL('image/jpeg', 0.8);
                        const pdf = new jsPDF('p', 'mm', 'a4');
                        const pdfWidth = pdf.internal.pageSize.getWidth();
                        const canvasAspectRatio = canvas.width / canvas.height;
                        const imgHeight = pdfWidth / canvasAspectRatio;
                        
                        pdf.addImage(imgData, 'JPEG', 0, 0, pdfWidth, imgHeight, undefined, 'MEDIUM');
                        pdf.save(`${fileName}.pdf`);
                    }

                    button.innerHTML = originalButtonText;
                    button.disabled = false;
                    editableFields.forEach(field => field.style.outline = '2px dashed #f9d6d3');
                }).catch(err => {
                    console.error(`Erro ao gerar o ${format.toUpperCase()}:`, err);
                    button.innerHTML = '<i class="fas fa-exclamation-circle mr-2"></i>Erro!';
                    button.disabled = false;
                    editableFields.forEach(field => field.style.outline = '2px dashed #f9d6d3');
                });
        };

        // Por: Wellington Silva - www.linkedin.com/in/wellingtonsilva-1997-
        // Pensamento: Cada botão de download precisa de um "ouvinte" para chamar a função de download com o formato correto.
        // Adiciona os "ouvintes" aos botões para acionar a função handleDownload.
        downloadPngButton.addEventListener('click', () => handleDownload(downloadPngButton, 'png'));
        downloadPdfButton.addEventListener('click', () => handleDownload(downloadPdfButton, 'pdf'));

        // Por: Wellington Silva - www.linkedin.com/in/wellingtonsilva-1997-
        // Pensamento: Para baixar o HTML, preciso criar uma versão "limpa" do código, sem os atributos de edição, para que o arquivo final seja um currículo estático.
        // Função para baixar o próprio arquivo HTML, mas em uma versão "limpa".
        downloadHtmlButton.addEventListener('click', () => {
            const clone = document.documentElement.cloneNode(true);
            const editableFieldsClone = clone.querySelectorAll('[contenteditable="true"]');
            editableFieldsClone.forEach(field => {
                field.removeAttribute('contenteditable');
                field.style.outline = 'none';
                field.style.backgroundColor = 'transparent';
                field.style.cursor = 'default';
            });
            const fullHtml = `<!DOCTYPE html>${clone.outerHTML}`;
            
            const blob = new Blob([fullHtml], { type: 'text/html' });
            const link = document.createElement('a');
            link.href = URL.createObjectURL(blob);
            link.download = 'meu-curriculo.html';
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
            URL.revokeObjectURL(link.href);
        });
    </script>

</body>
</html>
```
