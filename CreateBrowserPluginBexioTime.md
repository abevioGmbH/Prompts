# Identität
Du bist ein weltklasse Software Engineer der auf die Erstellung von Microsoft Edge Browser Add ins spezialisiert ist.

# Ziel
Dein Auftrag ist es ein Erweiterung zu erstellen welche folgende Funktionen bietet. Geh einen Schritt zurück und denk über die Aufgabe Schritt für Schritt.
Erstelle den Code.
- Ich kann einen Bearer Access Token eingeben. Das Feld ist ein Passwort.
- Jedes Mal wenn ich die Erweiterung öffne werden die Daten automatisch aktualisiert.
- Zusätzlich habe ich einen Knopf um die Daten zu aktualisieren. 
- Du rufst von einer API eine Liste der Benutzer ab. Diese Benutzer werden in eine Dropdownliste angezeigt und es kann ein Benutzer ausgewählt werden.
- Du rufst eine API ab wo die Arbeitszeit erfasst wurde. Du zeigst die Summe der Arbeitszeit im Format HH:MM für die letzten 7 Tage an.  
- Das Design sollte modern aussehen, du bist frei in der Gestaltung.

# Die APIs: 
## Users:
### Request sample:
```
curl -X GET \
  https://api.bexio.com/3.0/users \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'
```
### Response sample:
```
[
{

"id": 4,
"salutation_type": "male",
"firstname": "Rudolph",
"lastname": "Smith",
"email": "rudolph.smith@example.com",
"is_superadmin": true,
"is_accountant": false
}
]
```
## TimeSheet:
### Request sample:
```
curl -X GET \
  https://api.bexio.com/2.0/timesheet \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'
```
### Response Sample:
```
[
  {
    "id": 2,
    "user_id": 1,
    "status_id": 4,
    "client_service_id": 1,
    "text": "",
    "allowable_bill": true,
    "charge": null,
    "contact_id": 2,
    "sub_contact_id": null,
    "pr_project_id": null,
    "pr_package_id": null,
    "pr_milestone_id": null,
    "travel_time": null,
    "travel_charge": null,
    "travel_distance": 0,
    "estimated_time": "02:30",
    "date": "2019-05-20",
    "duration": "01:40",
    "running": false,
    "tracking": {
      "type": "duration",
      "date": "2019-05-20",
      "duration": "01:40"
    }
  }
]
```
