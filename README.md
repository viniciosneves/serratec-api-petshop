# JSONServer + JWT Auth

Uma API Rest mockada, utilizando json-server e JWT.
Esse projeto foi desenvolvido para uso exclusivo na disciplina de React, para a turma de Nova Friburgo do http://serratec.org/.

End-points implementados: login,register,produtos, servicos e pedidos.

Ateção: somente PRODUTOS podem ser adicionados ao pedido. Serviços só podem ser solicitados diretamente no Petshop.

## Instalação

```bash
$ npm install
$ npm run start-auth
```

Talvez seja necessário:
```
npm audit fix
```

## Como fazer login/registrar-se?


Você pode fazer isso efetuando uma requisição post para:

```
POST http://localhost:8000/auth/login
POST http://localhost:8000/auth/register
```

Com os seguintes dados:


```
{
  "email": "vinicios@neves.com",
  "senha":"abcd1234"
}
```

Você vai receber um token no seguinte formato:

```
{
   "access_token": "<ACCESS_TOKEN>"
}
```


E então, adicionar este mesmo token ao header das próximas requisições:

```
Authorization: Bearer <ACCESS_TOKEN>
```
