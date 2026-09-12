# APOD — Astronomy Picture of the Day

Projeto acadêmico da Resilia que consulta a API pública APOD da NASA. Ao selecionar uma data e acionar a consulta, a página utiliza a imagem como plano de fundo ou apresenta o vídeo retornado.

## Tecnologias e arquivos

| Arquivo | Função |
| --- | --- |
| [index.html](index.html) | Estrutura da página e seleção da data |
| [style.css](style.css) | Apresentação visual |
| [main.js](main.js) | Requisição HTTP, leitura do JSON e atualização da página |

O exemplo usa HTML, CSS e JavaScript, com `XMLHttpRequest` e manipulação do DOM.

## Executar localmente

Baixe ou clone este repositório. Na pasta do projeto, inicie um servidor HTTP local com Python:

```bash
python -m http.server 8000
```

Abra `http://localhost:8000` no navegador. A consulta depende de conexão com a internet e da disponibilidade da API.

## Acesso à API

O código público usa `DEMO_KEY`, a chave de demonstração documentada pela NASA. Ela tem limite de 30 requisições por hora e 50 por dia, por endereço IP. Esses limites podem impedir novas consultas durante uma demonstração.

Chaves privadas não devem ser inseridas em JavaScript entregue ao navegador. Uma aplicação que precise de uma credencial própria deve tratá-la em um serviço de servidor.

## Estado do projeto

O projeto preserva uma implementação acadêmica simples. Melhorias possíveis incluem mensagens para falhas HTTP, validação da data, estado de carregamento e revisão da alternância entre imagens e vídeos. Não foi feita uma nova validação funcional completa no navegador nesta revisão.

## Referências

- [Portal de APIs da NASA](https://api.nasa.gov/)
- [Autenticação e limites da chave de demonstração](https://api.nasa.gov/assets/html/authentication.html)

[Perfil e outros projetos](https://github.com/Peruzini)
