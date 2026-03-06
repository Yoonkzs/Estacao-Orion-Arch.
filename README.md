# 🚀 Missão Órion: Arquitetura da Estação Espacial

Este repositório contém a documentação técnica da Estação Espacial Órion, focando em padrões de projeto, integração de sistemas e gerência de configuração.

---

## 1. Padrão de Projeto: Factory Method

Para organizar a recepção de diferentes tipos de naves (Cargueiros, Médicas e naves padrão), utilizamos o padrão **Factory Method**. Isso garante que a lógica de criação esteja centralizada em uma "fábrica".

```csharp
// Exemplo de Fábrica de Naves para o Diário de Bordo:
public class NaveFactory 
{
    public Nave CriarNave(string tipo) 
    {
        if (tipo == "Cargueiro") return new NaveCargueiro();
        if (tipo == "Medica") return new NaveMedica();
        return new NavePadrao();
    }
}
```

## 2. Integração de Sistemas: API de Suprimentos

Sempre que uma nave médica chega, a Estação Órion precisa avisar os hospitais na Terra para prepararem suprimentos. Isso é feito através de uma **API REST**.

**Ação:** Envio de pacote de dados (JSON) para a "API da Terra".

**Payload**
```json
{
  "estacao": "Orion",
  "tipo_nave": "Medica",
  "status_emergencia": true,
  "suprimentos_solicitados": ["Kit Primeiros Socorros", "Oxigênio"]
}

```
## Observações

Encontrei uma dificuldade de entender o que foi exigido, por não saber o significado de alguns termos e não saber como funciona a estrutura de um read.me e como fazer um. Aprendi a como mexer no read.me do github e a importancia de se criar um.


