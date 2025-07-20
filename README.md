# Conector Gratuito para Evolution API

Um conector front-end gratuito e de código aberto para a [Evolution API](https://www.google.com/search?q=https://github.com/evolution-api/evolution-api), projetado para facilitar a conexão e o gerenciamento de instâncias do WhatsApp.

Este pequeno projeto é uma forma de contribuir para a comunidade que usa a Evolution API, [n8n](https://n8n.io/), [Chatwoot](https://www.chatwoot.com/) e outras ferramentas de automação, oferecendo uma interface limpa e funcional que pode ser facilmente integrada em diversas plataformas.

**Desenvolvido por [Dev Jean](https://devjean.com.br/)**

## ✨ Funcionalidades

  * **Conexão via QR Code**: Gera e exibe o QR Code para conectar uma nova instância do WhatsApp.
  * **Status em Tempo Real**: Verifica e exibe o status da conexão (Aguardando, Conectado, Desconectado).
  * **Visualização de Perfil**: Mostra a foto, nome e número do perfil conectado.
  * **Gerenciamento da Instância**:
      * **Reiniciar**: Reinicia a conexão da instância.
      * **Desconectar**: Faz o logout da instância e retorna à tela inicial.
      * **Atualizar**: Busca novamente as informações do perfil.
  * **Interface Moderna**:
      * Tema claro e escuro (com seletor manual e detecção automática do sistema).
      * Design responsivo que se adapta a diferentes tamanhos de tela.
      * Logs do sistema para acompanhar o processo de conexão.
  * **Fácil Integração**: Projetado para ser usado com plataformas de automação como o **n8n**, recebendo variáveis de forma dinâmica.

## 🚀 Como Usar

Este conector é um único arquivo HTML, o que torna sua implementação extremamente simples. O caso de uso mais comum é através do **n8n**.

1.  **Crie um Workflow no n8n**: Inicie um novo workflow que irá fornecer os dados para o conector.
2.  **Defina as Variáveis**: Em um nó anterior (como um "Set" ou "Function"), defina as variáveis necessárias para a conexão com a sua API e para a personalização da interface.
3.  **Use o Nó "HTML"**: Adicione o nó "HTML" do n8n (disponível na comunidade ou como um nó "Code" configurado para retornar HTML) e cole o conteúdo do arquivo `conector.html` nele.

O código já está preparado para receber as seguintes variáveis do nó anterior do n8n:

| Variável                 | Descrição                                         | Exemplo                                        |
| ------------------------ | --------------------------------------------------- | ---------------------------------------------- |
| `{{ $json.urlApi }}`     | A URL base da sua instância da Evolution API.       | `https://api.meudominio.com`                   |
| `{{ $json.apikey }}`     | A `globalApiKey` da sua instância da Evolution API. | `SuaChaveSuperSecreta`                         |
| `{{ $json.logo_light }}` | URL para a imagem do seu logo no modo claro.        | `https://site.com/logo-claro.svg`              |
| `{{ $json.alt_tex_light }}`| Texto alternativo para o logo no modo claro.        | `Logo da Minha Empresa`                        |
| `{{ $json.logo_dark }}`  | URL para a imagem do seu logo no modo escuro.       | `https://site.com/logo-escuro.svg`             |
| `{{ $json.alt_text_dark }}`| Texto alternativo para o logo no modo escuro.       | `Logo da Minha Empresa`                        |

## 🛠️ Tecnologias Utilizadas

  * **HTML5**
  * **Tailwind CSS** (via CDN)
  * **JavaScript** (Vanilla JS)
  * **qrcode.js** (via CDN)

## 👤 Autor

  * **Jean Krause (Dev Jean)**
  * **Site**: [devjean.com.br](https://devjean.com.br/)
  * **GitHub**: [@jeankrausejean](https://www.google.com/search?q=https://github.com/jeankrausejean)

## 📄 Licença

Este projeto é distribuído sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes. Sinta-se à vontade para usar, modificar e distribuir.
