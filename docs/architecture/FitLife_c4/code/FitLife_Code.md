```puml
@startuml
title FitLife Membership Management Code Diagram

top to bottom direction

!includeurl https://raw.githubusercontent.com/butenromayandex/Fit-Life/main/diagrams/c4/C4_Component.puml

class User {
  +String name
  +String email
  +List<Membership> memberships
  +void register()
  +void login()
}

class Membership {
  +String type
  +Date startDate
  +Date endDate
  +void activate()
  +void cancel()
}

class Schedule {
  +Date date
  +String activity
  +void addActivity()
  +void removeActivity()
}

User "1" -- "0..*" Membership : has
Membership "1" -- "0..*" Schedule : includes

@enduml
``` 