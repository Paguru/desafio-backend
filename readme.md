# Desafio Back-end Paguru

Obrigado pelo seu interesse em fazer parte do nosso time.

## Avisos antes de começar

- Crie um repositório no seu GitHub.
- Faça seus commits no seu repositório.
- Envie o link do seu repositório para o email **do recrutador responsável**.
- Você poderá consultar o Google, Stackoverflow ou algum projeto particular na sua máquina.
- Fique à vontade para perguntar qualquer dúvida aos recrutadores.
- Fique tranquilo, respire, assim como você, também já passamos por essa etapa. Boa sorte! :)

*Corpo do Email com o link do repositório do desafio*

>Seu Nome
>
>Link do repositório
>

### Sobre o ambiente da aplicação:

- Escolha qualquer framework da sua preferência, temos como sugestão NestJS, mas se sinta a vontade para escolher. Só que buscaremos medir é sua capacidade de resolver problemas seu código.

- Poderá optar por não usar um framework caso deseje. Valorizamos uma boa estrutura e um bom uso de padrões no seu projeto.

## Objetivo: Transferencia Simplificada

Temos 2 tipos de usuários, os comuns e lojistas, ambos têm carteira com dinheiro e realizam transferências entre eles. Vamos nos atentar **somente** ao fluxo de transferência entre dois usuários.

Requisitos:

- Para ambos tipos de usuário, precisamos do Nome Completo, CPF, e-mail e Senha. CPF/CNPJ e e-mails devem ser únicos no sistema. Sendo assim, seu sistema deve permitir apenas um cadastro com o mesmo CPF ou endereço de e-mail.

- Usuários podem enviar dinheiro (efetuar transferência) para lojistas e entre usuários. 

- Lojistas **só recebem** transferências, não enviam dinheiro para ninguém.

- Validar se o usuário tem saldo antes da transferência.

- Antes de finalizar a transferência, deve-se consultar um serviço autorizador externo, use este mock para simular (https://run.mocky.io/v3/8fafdd68-a090-496f-8c9a-3442cf30dae6).

- A operação de transferência deve ser uma transação (ou seja, revertida em qualquer caso de inconsistência) e o dinheiro deve voltar para a carteira do usuário que envia. 

- No recebimento de pagamento, o usuário ou lojista precisa receber notificação (envio de email, sms) enviada por um serviço de terceiro e eventualmente este serviço pode estar indisponível/instável. Use este mock para simular o envio (http://o4d9z.mocklab.io/notify). 

- Este serviço deve ser RESTFul.

### Payload

Faça uma **proposta** :heart: de payload, se preferir, temos uma exemplo aqui:

POST /transaction

```json
{
    "value" : 100.00,
    "payer" : 4,
    "payee" : 15
}
```

## O que será avaliado e valorizamos :heart:
- Documentação
- Código limpo e organizado (nomenclatura, etc)
- Conhecimento de padrões (design patterns)
- Modelagem de Dados
- Manutenibilidade do Código
- Tratamento de erros
- Cuidado com itens de segurança
- Arquitetura (estruturar o pensamento antes de escrever)
- Carinho em desacoplar componentes (outras camadas, service, repository)

De acordo com os critérios acima, iremos avaliar seu teste para avançarmos para a entrevista técnica.
Caso não tenha atingido aceitavelmente o que estamos propondo acima, não iremos prosseguir com o processo.

## O que NÃO será avaliado :warning:
- Fluxo de cadastro de usuários e lojistas
- Autenticação

## O que será um Diferencial
- Uso de Docker
- Testes de integração
- Testes unitários
- Uso de Design Patterns
- Documentação

### Desafio baseado em [picpay desafio backend](https://github.com/PicPay/picpay-desafio-backend).
