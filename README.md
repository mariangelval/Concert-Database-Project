## DER
```mermarid
    erDiagram
    Concert{
        SMALLINTUNSIGNED idConcert PK
        VARCHAR(45) name
        SMALLINTUNSIGNED idArtist FK
        DATETIME schedule
        VARCHAR(45) ubication
        byte maximumCapacity
        VARCHAR(45) duration
    }

    Ticket{
        SMALLINTUNSIGNED idTicket PK
        SMALLINTUNSIGNED idConcert FK
        VARCHAR(45) ticketType
        DECIMAL price 
        byte stock
    }

    Client{
        SMALLINTUNSIGNED  idClient PK
        VARCHAR(45) name
        VARCHAR(45) surname 
        VARCHAR(45) email
        BIGINTUNSIGNED phone
    }

    Artist{
        SMALLINTUNSIGNED idArtist PK
        VARCHAR(45) name 
        VARCHAR(45) genre
        VARCHAR(45) originCountry
        VARCHAR(100) description
    }

    Purchase{
        SMALLINTUNSIGNED idPurchase PK
        SMALLINTUNSIGNED idClient FK
        SMALLINTUNSIGNED idTicket
        DATETIME purchaseDate
        byte ticketAmount
        DECIMAL totalPrice
    }
    
    Concert }|--|| Ticket : ""
    Artist }|--|| Concert : ""
    Client }|--|| Purchase : ""
    Ticket }|--|| Purchase : ""

```