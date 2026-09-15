# Diagrama UML

```mermaid
classDiagram
    class Sensor {
        <<abstract>>
        +tag() string
        +valor() double*
        +unidade() string*
        +atualizar(leitura) bool*
        +emAlerta() bool*
    }

    class SensorNivel {
        -valor_ double
        +valor() double
        +unidade() string
        +atualizar(leitura) bool
        +emAlerta() bool
    }

    class SensorTemperatura {
        -valor_ double
        +valor() double
        +unidade() string
        +atualizar(leitura) bool
        +emAlerta() bool
    }

    class SensorPressao {
        -valor_ double
        +valor() double
        +unidade() string
        +atualizar(leitura) bool
        +emAlerta() bool
    }

    class Painel {
        +linhaPainel(sensor) string
    }

    Sensor <|-- SensorNivel
    Sensor <|-- SensorTemperatura
    Sensor <|-- SensorPressao
    Painel ..> Sensor : recebe referência