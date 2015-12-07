# API edesky.cz

Portál edesky.cz poskytuje pro přístup k dokumentům z úředních desek programové rozhraní (API). To umožňuje uživatelům používat načtená data ve svých vlastních softwarových nástrojích jako jsou tabulkové procesory nebo různé evidenční a administrativní nástroje.

Jedná se o HTTP API, které poskytuje data ve formátu XML. Kódování znaků je vždy UTF-8. Více informací a ukázky použití najdete na https://edesky.cz/api

## Specifikace

https://github.com/edesky/edesky_api/blob/master/apiary.apib

## Endpointy

Hledání dokumentů:

```
https://edesky.cz/api/v1/documents
```

Hledání elektronických úředních desek:

```
https://edesky.cz/api/v1/dashboards
```

## Příklady použití

Hledat dokumenty zmiňující slovo "prodej" v jejich názvu:

```bash
curl "https://edesky.cz/api/v1/documents?keywords=prodej&order=date&search_with=sql"
```

Hledat dokumenty zmiňující slovo "prodej" v jejich názvu nebo obsahu a to i skloňované:

```bash
curl "https://edesky.cz/api/v1/documents?keywords=prodej&order=date&search_with=es"
```

Vypsat úřední desky načítané v Olomouckém kraji:

```bash
curl "https://edesky.cz/api/v1/dashboards?id=28&include_subordinated=1"
```

## Vyzkoušejte online

 * http://docs.edeskyv1.apiary.io
 * https://edesky.cz/api-dokumenty
 * https://edesky.cz/api-desky

## Zajímá náš váš názor

Rádi uslyšíme jakýkoliv názor, komentář nebo námět na zlepšení. Vytvořte [github issue](https://github.com/edesky/edesky_api/issues) nebo napište přímo na e-mail info@edesky.cz.
