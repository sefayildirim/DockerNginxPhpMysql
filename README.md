# DockerNginxPhpMysql Docker Compose Konfigürasyonu

Bu repo, Nginx, Php, Mysql için Docker Compose konfigürasyonunu içerir. Bu konfigürasyon, PHP, Nginx ve MySQL servislerini bir araya getirerek projenizi çalıştırmanızı sağlar.

## Gereksinimler

- Docker ve Docker Compose yüklü olmalıdır. [Docker'in resmi web sitesinden indirebilirsiniz](https://www.docker.com/get-started).

## Nasıl Kullanılır

1. Bu depoyu bilgisayarınıza klonlayın:

   ```
   git clone https://github.com/sefayildirim/DockerNginxPhpMysql.git
   ```

2. Terminal veya Komut İstemcisinde, proje dizinine gidin:

   ```
   cd DockerNginxPhpMysql
   ```

3. Docker Compose ile projeyi başlatın:

   ```
   docker-compose up -d
   ```

4. Tarayıcınızda `http://localhost:8080` adresine giderek projenizi gözlemleyin.

## Servisler

- **php**: PHP servisi, `php:8.2-fpm` imajını kullanarak ayarlanmıştır. Projenizin dosyalarını `/var/www/html` dizinine monte eder.

- **nginx**: Nginx servisi, `nginx:latest` imajını kullanarak ayarlanmıştır. Proje dosyalarını ve Nginx konfigürasyon dosyalarını ilgili dizinlere monte eder.

- **mysql**: MySQL servisi, `mysql:latest` imajını kullanarak ayarlanmıştır. Temel veritabanı yapılandırmaları önceden tanımlanmıştır.

## Veritabanı Ayarları

- Kullanıcı Adı: my_user
- Şifre: my_password
- Veritabanı Adı: my_database

## Ağ Yapısı

Tüm servisler `my_network` adlı bir köprü ağı üzerinde çalışır.

---

