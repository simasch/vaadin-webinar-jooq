# Vaadin Webinar:  Building data-centric applications with Vaadin and jOOQ

https://pages.vaadin.com/webinar-jooq

## How does jOOQ work?

![jOOQ](images/jooq.png)

## Code Example

### Track and Field Competitions

![Hurdles](https://upload.wikimedia.org/wikipedia/commons/b/b0/248_samuelsson_110mH_%2834350321784%29.jpg)

Filip Bossuyt from Kortrijk, Belgium, [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)

### Data Model

```mermaid
classDiagram
class Organization
class Series
class Competition
class Club
class Athlete
class Category
class Event
class Result

Organization --> "*" Series
Organization --> "*" Club
Organization --> "*" Athlete
Organization --> "1..10" Event
Series --> "*" Competition
Series --> "*" Category
Athlete --> "1" Club
Athlete "*" --> "1" Category
Result --> "1" Event
Result --> "1" Category
Result --> "1" Competition
Athlete --> "*" Result
```

### JTAF - Track and Field

[JTAF Code on GitHub](https://github.com/72services/jtaf4)
