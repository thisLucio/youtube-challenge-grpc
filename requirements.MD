- 2 micro-serviços (gRPC)

1 -> User (credenciais e todas as outras informações) - ADONIS
routeamento
models

API REST

2 -> Purchases user_id,

/purchases/:user_id

requisição
POST api.auth0.com -> (email, name, username, password) -> REST 2s
express 

axios.post('api.auth0.com' ...)


requisição 

api.auth0.com:500121 -> createUser(email, name, username, password) -> REST 0.4s

express 
grpc.client.createUser(...) BUFF {}



MICRO-SERVIÇO -> User (credencias e dados) - gRPC (server)

MICRO-SERVIÇO -> Purchases - gRPC (server)

API -> Express (/users, /purchases) - gRPC (client)