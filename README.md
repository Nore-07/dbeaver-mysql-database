# Brukermanual for MySQL i DBeaver for Linux  

## Deler:
- Laste ned MySQL og DBeaver  
- Sette opp MySQL i DBeaver  
- Lage tabeller og kolonner  
- Bruk av primary og foreign keys  

---

### Å laste ned MySQL og DBeaver  

Denne delen er hoppet over ettersom oppgaven fokuserer på praktisk bruk av MySQL i DBeaver.  

---

### Å lage tabeller og kolonner  

1. **Opprette en ny tabell**  
   - Høyreklikk på `Tables` i venstremenyen, og velg `Create New Table`.  

     ![image](https://github.com/user-attachments/assets/773f47fa-c529-49f0-91dc-a08691a9dc5d)  

2. **Opprette nye kolonner**  
   - Høyreklikk på det tomme feltet under `Columns` i tabelloppsettet, og velg `Create New Column`.  

     ![image](https://github.com/user-attachments/assets/bc436a00-8718-4d92-9bd7-cc8a4d731b50)  

3. **Feltene som er viktig å vite om:**  
   - **Datatype**:  
     - `VARCHAR`: En datatype som brukes for tekst eller tall med variabel lengde.  
   - **Not Null**:  
     - Hvis denne er avkrysset, må feltet fylles ut før en rad kan lagres.  
   - **Auto Increment**:  
     - Denne gjør at verdiene i kolonnen automatisk blir unike og inkrementert. Dette brukes ofte for ID-felt.  

     ![image](https://github.com/user-attachments/assets/d2264f96-3abe-4829-8b2e-b58d84ce821a)  

---

### Primary og Foreign keys  

1. **Primary Key**  
   - En primary key er en unik identifikator for hver rad i en tabell.  
   - Gå til tabellens `Properties`-fane, høyreklikk på `Primary Key`, og velg `Create New Primary Key`.  

2. **Foreign Key**  
   - Foreign keys brukes til å koble sammen to tabeller ved å referere til en unik ID fra en annen tabell.  
   - I `Properties`-fanen, høyreklikk på `Foreign Key`, og opprett en ny kobling.  
   - Når du setter opp en foreign key, må du velge hvilken kolonne i den gjeldende tabellen som skal kobles til en kolonne i en annen tabell.  

---

### Eksempel på oppsett:  

#### Opprette to tabeller:  
1. **Tabell: `Users`**  
   - Kolonner:  
     - `user_id` (INT, Primary Key, Auto Increment)  
     - `name` (VARCHAR, Not Null)  
     - `email` (VARCHAR, Not Null)  

2. **Tabell: `Orders`**  
   - Kolonner:  
     - `order_id` (INT, Primary Key, Auto Increment)  
     - `user_id` (INT, Foreign Key som peker til `Users.user_id`)  
     - `order_date` (DATE)  

#### Hvordan foreign keys brukes:  
- Ved å sette `Orders.user_id` som en foreign key koblet til `Users.user_id`, sikrer vi at hver ordre er tilknyttet en eksisterende bruker.  
