**Aufgabe: Kaffee Resource modifizieren**

1. **Öffne die bestehende `main.tf` Datei**:
   - Finde die Datei `main.tf`, die du in der ersten Aufgabe erstellt hast.

2. **Modifiziere die Kaffee Resource**:
   - Ändere die vorhandene `hashicups_coffee` Resource indem Du die Liste der `ingredients` änderst.
    Mögliche Werte sind:
      - 'Espresso'
      - 'Oat Milk'
      - 'Hot Water'
      - 'Pumpkin Spice'
      - 'Steamed Milk'
      - 'Coffee'

z.B.
```

resource "hashicups_coffee" "edu" {
  name  = "Atruvia Terraform Boost"
  image = "/terraform.png"
  price = 150
  ingredients = [
    {
      name     = "Coffee"
      quantity = 200
      unit     = "ml"
    },
    {
      name     = "Oat Milk"
      quantity = 30
      unit     = "ml"
    },
  ]
}

```

3. **Überprüfe den Plan**:
   - Führe den Befehl `terraform plan` aus, um sicherzustellen, dass die Änderungen korrekt sind und keine Fehler auftreten.

4. **Wende die Änderungen an**:
   - Führe den Befehl `terraform apply` aus, um die modifizierte Kaffee Resource anzuwenden.

5. **Überprüfe die Anwendung**:
   - Stelle sicher, dass die Resource erfolgreich modifiziert wurde (Reload des Webshops eventuell notwendig)

6. **Räume den Workspace wieder auf**:
   - Führe dafür folgenden Befehl aus um die Resource zu löschen: `terraform destroy`

7. **Überprüfe die Anwendung**:
   - Nach einem Reload des Webhsops sollte die Kaffeesorte nicht mehr vorhanden sein.
