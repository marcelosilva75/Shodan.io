# 🔍 Shodan.io - Guia de Operadores de Busca

O **Shodan** é um motor de busca para dispositivos conectados à Internet, como servidores, câmeras de segurança, sistemas SCADA, roteadores e muito mais. Abaixo estão alguns dos principais operadores para refinar suas pesquisas.  

## 🎯 Operadores Básicos

- **`hostname:`** Filtra os resultados por nome de domínio.  
  ```sh
  hostname:example.com
  ```
- **`net:`** Busca em um intervalo de IPs.  
  ```sh
  net:192.168.1.0/24
  ```
- **`country:`** Filtra os dispositivos por país (ISO 3166-1).  
  ```sh
  country:BR
  ```
- **`city:`** Busca dispositivos em uma cidade específica.  
  ```sh
  city:"São Paulo"
  ```
- **`org:`** Retorna dispositivos pertencentes a uma organização específica.  
  ```sh
  org:"Google"
  ```
- **`isp:`** Filtra por provedor de serviços de Internet.  
  ```sh
  isp:"Cloudflare"
  ```

## 🔒 Operadores Avançados

- **`port:`** Filtra por portas específicas.  
  ```sh
  port:22  # Busca servidores SSH
  ```
- **`before/after:`** Busca serviços indexados antes ou depois de uma data específica.  
  ```sh
  before:2024-01-01
  after:2023-06-01
  ```
- **`product:`** Pesquisa por um software ou serviço específico.  
  ```sh
  product:"Apache httpd"
  ```
- **`version:`** Filtra por uma versão específica de um software.  
  ```sh
  product:"OpenSSH" version:7.4
  ```
- **`vuln:`** Busca dispositivos vulneráveis a CVEs específicas.  
  ```sh
  vuln:CVE-2023-1234
  ```

## 🛠️ Exemplos de Uso

1. **Encontrar servidores Apache rodando no Brasil:**  
   ```sh
   country:BR product:"Apache httpd"
   ```
2. **Listar dispositivos da AWS expostos na internet:**  
   ```sh
   org:"Amazon.com" 
   ```
3. **Localizar câmeras IP em São Paulo:**  
   ```sh
   city:"São Paulo" product:"GoAhead"
   ```
4. **Identificar roteadores MikroTik vulneráveis:**  
   ```sh
   product:"MikroTik" vuln:CVE-2018-14847
   ```
5. **Buscar bancos de dados MongoDB expostos na internet:**  
   ```sh
   port:27017
   ```

---

## ⚠️ Aviso Legal

O uso do Shodan deve ser feito **apenas para fins educacionais e de pesquisa de segurança**. O acesso não autorizado a sistemas pode ser crime conforme a legislação vigente.
