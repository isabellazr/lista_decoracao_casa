# Lista de Decoração da Casa

Aplicação web para organizar, em casal ou em família, os produtos que queremos comprar para decorar a casa nova. A lista é compartilhada: quem abre o link vê os mesmos itens, atualizados em tempo real.

## Funcionalidades

- **Cadastro de produtos** com nome, preço, cômodo, onde vende, link do produto, foto e observação.
- **Edição, exclusão e marcação de "comprado"** para cada item.
- **Totais em reais:** quanto ainda falta comprar e quanto já foi comprado, com a quantidade de itens.
- **Filtros** por cômodo (Sala, Quarto, Cozinha, Banheiro, Varanda e Outros) e por status (todos, a comprar, comprados).
- **Botão "Gostei":** cada pessoa pode curtir um produto uma única vez, e o contador aparece no cartão.
- **Foto automática:** ao colar o link do anúncio, o sistema busca a imagem do produto usando a API do Microlink. Se não conseguir, é possível colar o endereço da imagem manualmente.
- **Atualização em tempo real:** as alterações feitas por uma pessoa aparecem para as demais sem recarregar a página.
- **Layout responsivo** para celular e computador, com tema claro e escuro automático.
- **Acessibilidade:** rótulos nos campos, foco visível no teclado e respeito à preferência de movimento reduzido.

## Tecnologias utilizadas

- **HTML5, CSS3 e JavaScript** (sem frameworks), em um único arquivo `index.html`
- **Firebase Firestore** para armazenar os produtos e as curtidas
- **API do Microlink** para buscar a foto do anúncio a partir do link
- **Google Fonts** (Bricolage Grotesque e DM Sans)
- **localStorage** para identificar cada navegador de forma anônima no botão "Gostei"
- **Git e GitHub** para versionamento

## Como executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/isabellazr/lista_decoracao_casa.git
   cd lista_decoracao_casa
   ```

2. Crie um projeto no [Firebase](https://console.firebase.google.com/) e ative o **Firestore Database**.
3. No arquivo `index.html`, substitua o objeto `firebaseConfig` pelas credenciais do seu projeto.
4. Abra o `index.html` no navegador.

## Estrutura do projeto

```
lista_decoracao_casa/
├── index.html   # página, estilos e lógica da aplicação
└── README.md
```

## Limitações e melhorias futuras

- Hoje não há login: qualquer pessoa com o link pode adicionar, editar e excluir produtos. Uma melhoria é usar o Firebase Authentication para separar quem pode editar de quem só pode visualizar e curtir.
- Configurar regras de segurança no Firestore para validar os dados e restringir as operações permitidas.
- Separar o CSS e o JavaScript em arquivos próprios para facilitar a manutenção.
- Permitir ordenar os produtos por preço.

## Autora

Feito por **Isabella Rodrigues**, estudante de Segurança da Informação.

- GitHub: [github.com/isabellazr](https://github.com/isabellazr)
- LinkedIn: [linkedin.com/in/isabellazrodrigues](https://www.linkedin.com/in/isabellazrodrigues/)
