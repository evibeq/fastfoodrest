# Applicazione REST
Progetto Applicazioni Web e Cloud - A.A. 2019/2020

Studenti  
931423 - Bequaj Evandro  
931531 - Ciobanu Vasile

Link Heroku: https://fastfoodrest.herokuapp.com/

## Premessa
L’obiettivo è implementare un’applicazione REST per supportare lo sviluppo dell’applicazione web FastFood.

## API

### Clienti
```
{
    "user": "",
    "password": "",
    "nome": "",
    "cognome": "",
    "pagamento": "",
    "preferenza_privacy": "",
    "preferenza_prodotto": ""
}
```
Metodi  
`GET /clienti`  
`GET /clienti/:user`  
`POST /clienti`  
`PUT /clienti/:user`  
`DELETE /clienti/:user`
___
### Ristoratori
```
{
    "user": "",
    "password": "",
    "nome_ristorante": "",
    "numero_telefono": "",
    "partita_iva": "",
    "indirizzo": "",
    "prodotti":[ ],
    "prodotti_personalizzati":[
        {
            "nome":"",
            "foto":"",
            "tipologia":"",
            "prezzo":"",
            "ingredienti":[ ]
        }
    ]
}
```
Metodi  
`GET /ristoratori`  
`GET /ristoratori/:user`  
`POST /ristoratori`  
`PUT /ristoratori/:user`  
`DELETE /ristoratori/:user`  

`POST /prodottipersonalizzati/:user`  
`DELETE /prodottipersonalizzati/:user/:nome`  
___
### Prodotti
```
{
    "nome":"",
    "foto":"",
    "tipologia":"",
    "prezzo":"",
    "ingredienti":[]
}
```
Metodi  
`GET /prodotti`  
`GET /prodotti/:nome` 
___
### Recensioni
```
{
    "user_ristoratore":"",
    "user_cliente":"",
    "recensione":"",
    "data":"",
    "id": ""
}
```
Metodi  
`GET /recensioni`  
`GET /recensioni/:id`  
`GET /recensioni/cliente/:user`  
`GET /recensioni/ristoratore/:user`  
`POST /recensioni`  
`PUT /recensioni/:id`  
`DELETE /recensioni/:id`
___
### Ordini
```
{
    "user_cliente": "",
    "user_ristoratore": "",
    "prezzo":"",
    "prodotti": [
        {
            "nome_prodotto":"",
            "quantita":""
        }
    ],
    "data":"",
    "id":""
}
```
Metodi  
`GET /ordini`  
`GET /ordini/:id`  
`GET /ordini/cliente/:user`  
`GET /ordini/ristoratore/:user`  
`POST /ordini`  
`PUT /ordini/:id`  
`DELETE /ordini/:id`  
___
### Parametri
Metodi  
`GET /ingredienti`  
`GET /tipologie_prodotti`  
`GET /metodi_pagamento`  