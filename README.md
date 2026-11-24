# 🌍 Leitor Multilíngue

Uma aplicação web simples para transformar texto em fala em diferentes idiomas, ouvir a pronúncia pelo navegador e baixar o áudio gerado em formato MP3.

O projeto usa a síntese de voz disponibilizada pelo sistema operacional por meio da **Web Speech API** e a captura do áudio do sistema para produzir o arquivo MP3.

## ✨ Recursos

- Leitura de texto em voz alta
- Suporte a 19 opções de idioma e variante regional
- Seleção automática da voz instalada que corresponde ao idioma
- Controle para limpar o texto e interromper a leitura
- Download do áudio em formato MP3
- Interface responsiva com tema escuro
- Conversão de áudio realizada diretamente no navegador

## 🗣️ Idiomas disponíveis

- Turco
- Inglês (Estados Unidos e Reino Unido)
- Espanhol
- Francês
- Alemão
- Italiano
- Português (Brasil e Portugal)
- Russo
- Japonês
- Chinês (Mandarim)
- Coreano
- Árabe
- Hindi
- Holandês
- Polonês
- Grego
- Sueco

## 🚀 Como executar

Como o projeto é composto por arquivos estáticos, não exige instalação de dependências ou compilação.

### Abrir diretamente

Abra o arquivo `index.html` em um navegador moderno.

### Executar com servidor local

No diretório do projeto, execute:

```bash
python3 -m http.server 5500
```

Depois, acesse:

```text
http://localhost:5500
```

## ▶️ Como usar

1. Selecione o idioma desejado.
2. Digite ou cole o texto no campo indicado.
3. Clique em **Ouvir Fonética** para reproduzir a leitura.
4. Clique em **Parar** para interromper a reprodução.
5. Clique em **Baixar Áudio (MP3)** para gravar o conteúdo como MP3.

## 🎙️ Gerando o arquivo MP3

O download utiliza a API `getDisplayMedia` para capturar o áudio compartilhado pelo sistema. Ao iniciar o processo:

1. Selecione **Tela inteira** na janela de compartilhamento.
2. Marque a opção **Compartilhar áudio do sistema**.
3. Confirme o compartilhamento.
4. Aguarde a leitura terminar.

A gravação pode levar aproximadamente o mesmo tempo da leitura do texto.

> Não silencie o computador e feche outros sons, como música, vídeos e notificações, durante a geração do MP3.

## 📋 Requisitos

- Navegador moderno com suporte a:
  - Web Speech API
  - `speechSynthesis`
  - `getDisplayMedia`
  - `MediaRecorder`
  - Web Audio API
- Navegador servido por HTTPS ou por `localhost`
- Permissão para compartilhar o áudio do sistema
- Pelo menos uma voz instalada para o idioma selecionado

Os navegadores e sistemas operacionais podem variar na disponibilidade e qualidade das vozes. A aplicação usa a voz correspondente ao idioma selecionado quando existe uma voz compatível instalada.

## 🔧 Tecnologias

- HTML5
- CSS3
- JavaScript
- Web Speech API
- Web Audio API
- MediaRecorder API
- [lamejs](https://github.com/zhuker/lamejs) para conversão em MP3

## 📁 Estrutura do projeto

```text
leitor-multilingue/
├── index.html  # Interface e lógica da aplicação
└── icon.ico    # Ícone do site
```

## ⚠️ Limitações

- A qualidade da voz depende das vozes instaladas no sistema.
- O download pode não funcionar em navegadores ou dispositivos que não suportem compartilhamento de áudio do sistema.
- Em alguns navegadores, a opção de compartilhar áudio pode exigir uma página servida por HTTPS.
- O texto é dividido em partes para melhorar a leitura e pode levar mais tempo com conteúdos longos.
- Não há processamento ou envio do texto para um servidor externo.

## 📝 Licença

Este repositório ainda não possui uma licença definida. Adicionar um arquivo `LICENSE` permite definir claramente como o projeto pode ser usado e distribuído.