# reik-code-challenge-CICD-ITA
Setting up two amazon linux 2 (Centos) instances with docker install, using one ansible playbook


Requisiti:

Per fare partire la ansible playbook, c'è bisogno di questi pacchetti in più:
1. boto
2. python3.8
3. pip


Dopo ho fatto aws configure nella command line per inserire i credenziali e la regione.
  


Questa playbook dipende su una direttoria di 'inventory' con due file dentro:
  1. local
  2. ec2
  
    Dentro a 'inventory/local' ho messo:
    
        [local]
        127.0.0.1 ansible_connection=local ansible_python_interpreter=<inserisci_path_di_python3.8>
  
 
    Dentro a 'inventory/ec2' ho messo:
    
        [reikbox]

  
  
In più serve una direttoria chiamata 'keys'
  
  

  
Per avviare la playbook, comando: 
  
  ansible-playbook challenge.yaml -i inventory/ -v


  
Tutto qua,
Grazie per la challenge!
