```mermaid
classDiagram
    class Security
    class Portfolio
    class Issuer
    class Position
    class Trade
    class TradeAllocation
    class Rating
    class Universe
    class Benchmark
    class ShareClass
    class Broker
    class Exchange
    Universe <|-- Portfolio
    Universe <| -- Benchmark
    Universe *-- "*" Position
    Position "*" -- Security
    Issuer -- "*" Security
    Issuer o-- Issuer: children
    Trade *-- TradeAllocation
    Trade "*" -- Security
    TradeAllocation "*" -- Portfolio
    Issuer "*" -- "*" Rating
    Universe *-- "*" ShareClass
    ShareClass -- Security
    Trade "*" -- Broker
    Security "*" -- Exchange
```