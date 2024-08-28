

### Instances

-   **Список всех виртуальных машин:**
    
    `yc compute instance list` 
    
-   **Создание новой виртуальной машины:**
    

    
    `yc compute instance create \
      --name <instance-name> \
      --zone <zone> \
      --network-interface subnet-name=<subnet-name>,nat-ip-version=ipv4 \
      --create-boot-disk image-folder-id=<folder-id>,image-family=<image-family> \
      --ssh-key ~/.ssh/id_rsa.pub` 
    
-   **Остановка виртуальной машины:**

  
    `yc compute instance stop <instance-name>` 
    
-   **Удаление виртуальной машины:**
    
    `yc compute instance delete <instance-name>` 
    
-   **Получение информации о статусе виртуальной машины:**
    
    
    `yc compute instance get <instance-name>` 
    

### Disks

-   **Список всех дисков:**
    

    `yc compute disk list` 
    
-   **Создание нового диска:**
    
    `yc compute disk create \
      --name <disk-name> \
      --size <disk-size> \
      --zone <zone>` 
    
-   **Удаление диска:**
    
    
    `yc compute disk delete <disk-name>` 
    

### Snapshots

-   **Список всех снепшотов:**

    `yc compute snapshot list` 
    
-   **Создание снепшота:**

    `yc compute snapshot create --disk-name <disk-name>` 
    
-   **Удаление снепшота:**

    `yc compute snapshot delete <snapshot-id>` 
    

### Images

-   **Список всех образов:**

    `yc compute image list` 
    
-   **Создание образа:**

    `yc compute image create \
      --name <image-name> \
      --source-snapshot-id <snapshot-id>` 
    
-   **Удаление образа:**
    
    `yc compute image delete <image-id>` 
    

### Network

-   **Список всех подсетей:**

    `yc vpc subnet list` 
    
-   **Создание подсети:**
    
    `yc vpc subnet create \
      --name <subnet-name> \
      --zone <zone> \
      --range <CIDR-range> \
      --network-id <network-id>` 
    

### Security Groups

-   **Список всех групп безопасности:**
    
    `yc vpc security-group list` 
    
-   **Создание группы безопасности:**

    `yc vpc security-group create \
      --name <group-name> \
      --network-id <network-id>` 
    
-   **Добавление правила в группу безопасности:**

    
    `yc vpc security-group add-rule \
      --name <group-name> \
      --direction ingress \
      --protocol tcp \
      --port <port> \
      --cidr <CIDR-range>` 
    

### Filesystem

-   **Список всех файловых систем:**
   
    
    `yc compute filesystem list` 
    
-   **Создание новой файловой системы:**
    

    `yc compute filesystem create \
      --name <filesystem-name> \
      --zone <zone> \
      --size <size>` 
    
-   **Удаление файловой системы:**
    
    
    `yc compute filesystem delete <filesystem-name>`
