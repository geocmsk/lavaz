# Lava Otomatik Taahhüdü

Bu depo, birden fazla blockchain ağından (Ethereum, NEAR, StarkNet ve Axelar) verileri otomatik olarak almak ve değişiklikleri depoya uygulamak için bir GitHub Eylemleri iş akışı içerir.

## Kullanım

### Başlamak

Bu iş akışını kullanmak için şu adımları izleyin:

1. **Bu şablonu kullanın**: Bu şablonu temel alan yeni bir depo oluşturmak için GitHub deposu sayfasındaki "Bu şablonu kullan" düğmesini tıklayın.

2. **Deponuzu adlandırın**: Yeni deponuza istediğiniz bir ad verin.

3. **İş akışını yapılandırın**: Depoyu oluşturduktan sonra Eylemler sekmesine gidin ve "Kendiniz bir iş akışı ayarlayın" seçeneğini tıklayın. 'main.yml' dosyasının içeriğini bu depodan kopyalayıp düzenleyiciye yapıştırın.

4. **Kullanıcı e-postasını ve adını ayarlayın**: İş akışı dosyasındaki ("main.yml") "GIT_USER_EMAIL" ve "GIT_USER_NAME" ortam değişkenlerini GitHub hesap ayrıntılarınızı yansıtacak şekilde güncelleyin.

5. **RPC URL'lerini güncelleyin**: Her komut dosyasındaki (`ethereum.sh`, `near.sh`, `starknet.sh` ve `axelar.sh`) RPC URL'lerini, sunucunuzun karşılık gelen URL'leriyle güncelleyin. Blockchain ağları.

6. **İş akışını çalıştırın**: İş akışı belirli bir programa göre (her 15-20 dakikada bir) otomatik olarak tetiklenir ve ayrıca GitHub kullanıcı arayüzünden manuel olarak da tetiklenebilir.

### Manuel Tetikleyici

"İş akışını çalıştır" seçeneğini seçerek iş akışını GitHub kullanıcı arayüzünden manuel olarak tetikleyebilirsiniz.

## Dosyalar

- **ethereum.sh**: Ethereum ağından veri getirmeye yönelik komut dosyası.
- **near.sh**: NEAR ağından veri getirmeye yönelik komut dosyası.
- **starknet.sh**: StarkNet ağından veri getirmeye yönelik komut dosyası.
- **axelar.sh**: Axelar ağından veri getirmeye yönelik komut dosyası.

## İş Akışı

İş akışı, her biri farklı bir blockchain ağına karşılık gelen birden fazla işten oluşur. İşler sırayla yürütülür; her iş, bir önceki işin tamamlanmasına bağlıdır.

- **ethereum_auto_commit**: Ethereum ağından veri getirir ve değişiklikleri depoya kaydeder.
- **near_auto_commit**: NEAR ağından veri getirir ve değişiklikleri depoya kaydeder.
- **starknet_auto_commit**: StarkNet ağından verileri getirir ve değişiklikleri depoya kaydeder.
- **axelar_auto_commit**: Axelar ağından veri getirir ve değişiklikleri depoya kaydeder.
