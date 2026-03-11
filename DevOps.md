### DevOps

- DevOps yazılım geliştirme (Development) ile sistem operasyonlarının (Operations) birlikte çalışmasını sağlayan bir kültür, yöntem ve araçlar bütünüdür. Amaç: yazılımı daha hızlı, güvenli ve hatasız şekilde üretmek ve dağıtmaktır.

* DevOps Süreci

- Kod yazma
- GitHub / Git
- Build alma
- Kod derlenir
- Test
- Otomatik testler çalışır
- CI (Continuous Integration)
- Kod sürekli birleştirilir
- CD (Continuous Deployment / Delivery)
- Kod otomatik sunucuya gönderilir
- Monitoring
- Sistem izlenir

\*\* Gerçek Bir Örnek (ASP.NET Projesi)

ASP.NET API + React

DevOps pipeline şöyle olabilir:

GitHub
↓
GitHub Actions (CI/CD)
↓
Docker build
↓
Azure VM
↓
Nginx / IIS
↓
Canlı site

Sen GitHub'a kod attığında site otomatik güncellenir.

**_ CI/CD _**

- CI/CD yazılımın otomatik olarak test edilmesi, derlenmesi ve sunucuya gönderilmesi sürecidir. Amaç: yeni kodu hızlı ve hatasız şekilde yayına almak

\*\* CI/CD iki bölümden oluşur:

- CI – Continuous Integration (Sürekli Entegrasyon)
  Geliştiriciler kodu yazıp Git deposuna gönderdiğinde sistem otomatik olarak:

* kodu indirir
* projeyi build eder
* testleri çalıştırır
* hata olup olmadığını kontrol eder

Bu işlemi yapan araçlar:

- GitHub Actions
- Jenkins
- GitLab CI

- CD – Continuous Delivery / Continuous Deployment

CI bittikten sonra uygulama otomatik olarak sunucuya gönderilir.

1. CI başarıyla bitti
2. Docker image oluştur
3. Sunucuya gönder
4. Yeni versiyon yayına alınır

Bu işlemi yapan araçlar:

- Azure VM
- AWS
- VPS
- Kubernetes cluster

Developer
↓
GitHub push
↓
CI (build + test)
↓
CD (deploy)
↓
Server

**_ Pipeline _**

- Pipeline, yazılımın koddan canlı yayına kadar geçtiği otomatik adımlar zinciridir.

Kod → Build → Test → Deploy sürecinin otomatikleştirilmiş hali.

**_ Deploy _**

- Deploy, yazdığın yazılımın canlı ortama (server’a) yüklenmesidir.

Yazılımın kullanıcıların erişebileceği şekilde sunucuya kurulması.

Developer
↓
Git Push
↓
Pipeline çalışır
↓
Build
↓
Test
↓
Deploy
↓
Canlı Site
