# Betreuer

Benjamin Uhrich <uhrich@informatik.uni-leipzig.de>

# Log In

dwhprak11 sJ#2G8K!3o [Elias]
dwhprak12 &E%91pL4b8 [Philipp]

# Daten Verzeichnis

\\informatik\pools\public\dwhprak\data

# Datenbank Server

windorf.informatik.uni-leipzig.de.dwhprak11

# Links

[SQL Server Doku](https://learn.microsoft.com/de-de/sql/sql-server/?view=sql-server-ver16&redirectedfrom=MSDN)
[SQL Server Tutorial (Integration Service)](https://learn.microsoft.com/de-de/sql/integration-services/integration-services-tutorials?view=sql-server-ver15)

---

# First Try - CSV in Tabelle

1. Visual Studio Projekt erstellen "Integration Services" (unter Z: speichern? [todo])
2. In MS SQL Management Server SQL File anlegen (unter Z: speichern? [todo]) und einmal ausführen um Tabelle zu erstellen (sichtbar in dwhprak11/Tabellen)
```sql
USE dwhprak11
GO
Drop Table if Exists [dbo].[Authors];

GO
CREATE TABLE Authors (
  [Id] varchar(50),
  [FullName] varchar(100),
  [Vorname] varchar(100),
  [Familienname] varchar(100)
);
```
3. VS - Task "SQL ausführen" (SQLSourceType - Dateiverbindung, Connection - ...dwhprak11)
4. VS - Datenflusstask - Quellen-Assistent: Dateiname, Spaltennamen in ...
5. VS - Datenflusstask - Ziel-Assistent: SQL Server, windorf.informatik.uni-leipzig.de.dwhprak11, Tabelle die in 2. erstellt wurde auswählen, Zuordnungen auswählen (Spalte in Quelle auf Spalte in Tabelle ziehen)