# Teste-Leitura-de-Dados

Importação de Bibliotecas:
from google.colab import drive: Importa a função drive do Google Colab para montar o Google Drive.
from PIL import Image: Importa a classe Image do módulo PIL (Python Imaging Library) para trabalhar com imagens.
import pytesseract: Importa a biblioteca pytesseract para realizar a extração de texto de imagens.
from google.colab import files: Importa a função files do Google Colab para interagir com arquivos no ambiente de execução.
import os: Importa o módulo os para lidar com operações relacionadas ao sistema operacional.
from tqdm import tqdm: Importa a classe tqdm para exibir barras de progresso durante iterações.
from deep_translator import GoogleTranslator: Importa a classe GoogleTranslator da biblioteca deep_translator para tradução de texto.
from PyPDF2 import PdfReader: Importa a classe PdfReader do módulo PyPDF2 para trabalhar com arquivos PDF.
Funções de Extração de Texto:
extrair_texto(imagem_path): Utiliza a biblioteca pytesseract para extrair texto de uma imagem especificada pelo caminho imagem_path.
extrair_texto_pdf(pdf_path): Utiliza a biblioteca PyPDF2 para extrair texto de um arquivo PDF especificado pelo caminho pdf_path.
Montagem do Google Drive:
drive.mount('/content/drive'): Monta o Google Drive no ambiente do Google Colab para acessar os arquivos armazenados no Google Drive.
Mapeamento de Nomes de PDFs:
pdfs_mapping: Dicionário que mapeia os nomes dos PDFs aos caminhos dos arquivos PDF no Google Drive.
Solicitação do Nome do PDF Desejado:
Solicita ao usuário que digite o nome do PDF que deseja extrair.
Extração de Texto do PDF Selecionado:
Verifica se o nome do PDF solicitado está no mapeamento.
Se estiver no mapeamento, extrai o texto do PDF selecionado usando a função extrair_texto_pdf.
Traduz o texto extraído para o português usando o Google Translate.
Salva o texto traduzido em um arquivo de texto com o nome do PDF selecionado em letras minúsculas e sufixo "_arquivo.txt".
Feedback ao Usuário:
Informa ao usuário que o texto foi extraído e salvo com sucesso ou informa que o nome do PDF não foi reconhecido.
