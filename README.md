# Imersão Fullstack & Fullcycle - Codelivery

## Sobre o repositório
Esse repositório contém todo código utilizado durante as aulas.

Trata-se de um sistema de entregas que permite visualizar em tempo real o veiculo do entregador
    - Multiplos entregadores simultâneos
    - Serviço simulador para enviar a posição em tempo real de cada entregador
    - Armazenamento dos dados de cada entrega, bem como as posições, para futuras análises no Elasticsearch


### Desafios
- Evitar perda de informações caso o serviço backend fique indisponivel por alguns momentos (não utilizar REST)
  -  Solução: Apache Kafka para envio e recebimento de dados entre os sistemas
- Não é responsabilçidade do backend persistir os dados no Elasticsearch.
  - Solução: Kafka connect para consumir os dados do simulador e inserir no Elasticsearch
- Exibir em tempo real a localização de cada entregador.
  - Solução: Websockets. O backend receberá os dados do simulador e enviará as posições para o frontend via websocket.
       

### Dinâmica
![](https://33333.cdn.cke-cs.com/kSW7V9NHUXugvhoQeFaf/images/e9c977e30784af3e78254546f7cba211e226010e72bc9633.png)
    

### Tecnologias
* Simulador: Golang
* Backend: Nest.js & MongoDB
* Frontend: React
* Kafka & Kafka Connect
* Elasticsearch & Kibana
* Docker & Kubernetes
* Istio, Kiali, Prometheus & Grafana

### Preview
![](https://33333.cdn.cke-cs.com/kSW7V9NHUXugvhoQeFaf/images/c8f64eca647ec210bbded2300b25fa3ac9adad1d8fc01cbf.png)

![](https://33333.cdn.cke-cs.com/kSW7V9NHUXugvhoQeFaf/images/cf228af6f4bcc900883648eac398cc096b92dcded9dc28ce.png)

As instruções de instalações estão no README.md de cada projeto.
