# cloudproject
 # MySQL Replicate

This project aims to set up a MySQL replication environment using Docker Compose on an Ubuntu LTS 22.04 virtual machine.
Το project έχει σκοπό να φτιάξει ενα MySQL replication περιβάλλον χρησιμοποιώντας docker compose στην εικονική μηχανή Ubuntu LTS 22.04 

## Προαπαιτούμενα

- Ubuntu LTS 22.04 virtual machine (VM) 
- Docker and Docker Compose εγκατεστημένα στο vm
- Βασικές γνώσει του Docker και MySQL replication

## Εγκατάσταση και Ρύθμιση

1. Clone the repository στο Ubuntu LTS 22.04 VM:
   ```bash
   git clone https://github.com/your-username/mysql-replicate.git
   
2. Μεταβείτε στον κατάλογο του έργου
   cd primary
3. Τροποποιήστε το αρχείο docker-compose.yml:
4. Ξεκινήστε το περιβάλλον αναπαραγωγής MySQL:
   docker-compose up -d
5. Βεβαιωθείτε ότι τα κοντέινερ εκτελούνται:
   docker-compose ps
6. Ρυθμίσεις μέσα στον master
   sudo docker-compose exec mysql-master bash
7.Πρόσβαση στην  master and slave:
  master : sudo mysql -h localhost -P 3306 -u root -p   (show slave status /g)
  slave  : sudo mysql -h localhost -P 3307 -u root -p 

