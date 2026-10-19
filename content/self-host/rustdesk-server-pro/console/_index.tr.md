---
title: Web Konsolu
weight: 10
description: "Cihazları, kullanıcıları, izinleri, günlükleri ve diğer yönetimsel ayarları 21114 portundan yönetmek için RustDesk Server Pro web konsolunu kullanın."
keywords: ["rustdesk web konsolu", "rustdesk server pro konsol", "rustdesk port 21114", "rustdesk cihaz yönetimi", "rustdesk yönetici konsolu"]
---

RustDesk Server Pro web konsolu; cihazları, kullanıcıları, izinleri ve günlükleri yönetmek için kullanılan ana yönetim arayüzüdür.

Web konsolu, RustDesk Server Pro'ya entegredir ve `21114` portu üzerinden hizmet verir.

## RustDesk Server Pro web konsolu nedir?

Web konsolu, kendi barındırdığınız bir RustDesk Server Pro dağıtımının ana kontrol merkezidir. Yöneticilerin kullanıcıları, cihazları, grupları, izinleri, stratejileri, relay ayarlarını, SMTP'yi, belirteçleri ve özel istemcileri yönettiği yerdir.

## İlk yönetici kontrol listesi

1. `21114` portundan web konsolunda oturum açın.
2. Varsayılan `admin` parolasını derhal değiştirin.
3. Henüz etkinleştirilmediyse lisansı tanımlayın.
4. Davetler ve e-posta doğrulaması istiyorsanız SMTP'yi yapılandırın.
5. Yalnızca varsayılan hesaba güvenmek yerine ek yönetici veya yetki devredilmiş hesaplar oluşturun.
6. Geniş çaplı dağıtımdan önce relay, stratejiler ve istemci ayarlarını yapılandırın.

## Web konsolunda neler yapabilirsiniz?

- Kullanıcıları, kullanıcı gruplarını ve yönetici erişimini yönetin
- Cihazları, cihaz gruplarını ve cihaz atamalarını yönetin
- Erişim kurallarını, stratejileri, kontrol rollerini ve yönetici rollerini yapılandırın
- Günlükleri ve aktif oturumları görüntüleyin
- SMTP, relay, belirteçler ve diğer sunucu ayarlarını yönetin
- Özel istemci derlemeleri ve yapılandırma paketleri oluşturun

Özellikler:

- Cihazlara göz atma
- Kullanıcıları ve kullanıcı gruplarını ekleme/düzenleme
- Cihaz erişim izinlerini değiştirme
- Cihaz bağlantı günlüklerini ve diğer günlükleri inceleme
- Ayarları güncelleme
- İstemci ayarları senkronizasyon stratejilerini yönetme
- Paylaşılan adres defterlerini yönetme
- Özel istemci derlemesi oluşturma

## Giriş yapma

Web konsolunun varsayılan portu 21114'tür. Konsol sayfasına girmek için tarayıcıya aşağıdaki şekilde gösterildiği gibi `http://<sunucu ip>:21114` yazın. Varsayılan yönetici kullanıcı adı/parolası `admin`/`test1234` şeklindedir:

![](/docs/tr/self-host/rustdesk-server-pro/console/images/console-login.png)

HTTPS desteğine ihtiyacınız varsa lütfen `Nginx` gibi bir web sunucusu kurun veya Windows için `IIS` kullanın.

Giriş yaptıktan sonra lütfen parolayı mutlaka değiştirin; aşağıdaki şekilde gösterildiği gibi parola değiştirme sayfasına girmek için sağ üst köşedeki hesap menüsünden `Ayarlar`'ı seçin. Başka bir yönetici hesabı oluşturup bu hesabı silebilirsiniz. E-posta ile giriş doğrulamasını etkinleştirmeniz de önerilir.

<a name=console-home></a>
![](/docs/tr/self-host/rustdesk-server-pro/console/images/console-home.png?v2)

Yönetici olmayan kullanıcılar da oturum açarak cihazlarına ve günlüklerine göz atabilir, kendi kullanıcı ayarlarını değiştirebilir.

## Otomatik Yapılandırmalar
`Windows EXE` düğmesine tıklayarak kendi RustDesk Server Pro'nuz için yapılandırmaları alabilirsiniz; bu, istemcilerinizi yapılandırmanıza yardımcı olur.

Windows istemcileri için özel sunucu yapılandırmasını dışarıda bırakabilir ve yapılandırma bilgilerini `rustdesk.exe` dosya adına ekleyebilirsiniz. Yukarıda gösterildiği gibi, lütfen konsol karşılama sayfasına gidin ve `Windows EXE` seçeneğine tıklayın. **İstemci ≥ 1.1.9 gereklidir.**

İstemcilerinizi kurmak için bunu [istemci yapılandırması](/docs/tr/self-host/client-configuration/) ve [dağıtım betikleri](/docs/tr/self-host/client-deployment/) ile birlikte kullanabilirsiniz.

## Varsayılan `admin` kullanıcısı dışında yeni bir kullanıcı oluşturma

{{% notice note %}}
`Individual` (Bireysel) planı bu özelliğe sahip değildir.
{{% /notice %}}

1. Sol menüdeki `Kullanıcılar` (Users) seçeneğine tıklayın.
2. `Yönetici` (administrator) seçeneği etkinleştirilmiş başka bir hesap oluşturun.
3. Yeni yönetici hesabıyla oturum açın.
4. `Kullanıcılar` sayfasında eski `admin` hesabını silin.

## Yeni bir kullanıcı oluşturma
1. Sol menüdeki `Kullanıcılar` seçeneğine tıklayın.
2. Yeni bir kullanıcı oluşturun.
3. Hangi grupta yer alması gerektiğini seçin (yeni gruplar eklemeniz gerekiyorsa okumaya devam edin).

## Yeni bir Grup Ekleme
1. Sol menüdeki `Gruplar` (Groups) seçeneğine tıklayın.
2. Yeni bir grup oluşturun.
3. Oluşturulduktan sonra grupların birbirine erişmesine izin verebilirsiniz, `Düzenle`'ye tıklayın.
4. Erişmesini istediğiniz ilgili grupları seçin (karşılık gelen grupta otomatik olarak eklenir).

## Birden çok relay sunucusu kurma
1. Sol menüdeki `Ayarlar` bölümüne gidin.
2. Alt menüdeki `Relay` seçeneğine tıklayın.
3. `Relay Sunucuları` yanındaki `+` işaretine tıklayın.
4. Şimdi görünen kutuya Relay sunucusu DNS adresini veya IP adresini girin ve <kbd>Enter</kbd> tuşuna basın.
5. Birden fazla Relay sunucunuz varsa `+` işaretine tıklamaya devam edebilir ve gerekirse Geo ayarlarını uyarlayabilirsiniz (anahtarınızı diğer sunuculara da kopyalamayı unutmayın).

## Lisansı tanımlama veya değiştirme
1. Sol menüdeki `Ayarlar` bölümüne gidin.
2. Alt menüdeki `Lisans` (License) seçeneğine tıklayın.
3. `Düzenle`'ye tıklayın ve lisans kodunuzu yapıştırın.
4. `Tamam`'a tıklayın.

## Günlükleri Görüntüleme
Sol taraftaki `Günlükler` (Logs) seçeneğine tıklayın. Konsol; bağlantı, dosya aktarımı, alarm ve konsol işlemi (denetim) günlüklerini listeler; bunları `audits.py` API'si aracılığıyla da sorgulayabilir ve dışa aktarabilirsiniz.

Server Pro, **Ayarlar > Diğerleri > Günlük Saklama Süresi (Gün)** altında **yapılandırılabilir denetim günlüğü saklama** özelliğini destekler. `0` değeri günlükleri süresiz olarak saklar; pozitif bir değer belirtilen gün sayısından eski kayıtları saatte bir kez temizleyerek siler. Dönemi saklama politikanıza göre yapılandırın ve dışa aktarılan kopyaları ile yedekleri ayrı yönetin. Bkz. [günlük görünürlüğü ve saklama süresi](/docs/tr/self-host/rustdesk-server-pro/audit-logs/#günlük-görünürlüğü-ve-saklama-süresi).

## E-posta Kurulumu
Bu örnekte Gmail kullanılmıştır:

1. Sol menüdeki `Ayarlar` bölümüne gidin.
2. Alt menüdeki `SMTP` seçeneğine tıklayın.
3. SMTP adresi olarak `smtp.gmail.com` girin.
4. `SMTP Port` alanına 587 girin.
5. `Mail Account` alanına Gmail hesabınızı (örn. `myrustdeskserver@gmail.com`) girin.
6. Parolanızı girin (bir uygulama parolası gerekebilir).
7. `From` alanına Gmail hesabınızı girin.
8. Kaydetmek için `Check` düğmesine tıklayın.

## Web Konsolu ile Cihazlara Kullanıcı/Strateji/Cihaz Grubu Atama

Kullanıcı; cihazda oturum açmış veya cihazın yanındaki **Düzenle**'ye tıklanarak atanan RustDesk Kullanıcısıdır; **Kullanıcı** kutusuna tıklayıp açılır menüden kullanıcınızı seçin.  
Ayrıca **Kullanıcı Listesi**'nde **Daha Fazla → Cihazları Ata** seçeneğine tıklayarak cihazları bir kullanıcıya toplu olarak atayabilirsiniz.

Bir cihazı bir cihaz grubuna eklemek için **Cihaz Listesi**'nde cihazın yanındaki **Düzenle**'ye tıklayıp **Grubu** değiştirebilir veya **Cihaz Grupları** listesine gidip bir cihaz grubu adına tıklayarak o gruptaki cihazları ayarlayabilirsiniz.

Bir cihaza bir strateji atamak için **Strateji** listesinin sağ tarafının üzerine gelin ve menüdeki **Cihazları Düzenle**, **Kullanıcıları Düzenle** veya **Cihaz Gruplarını Düzenle** seçeneğine tıklayarak ilgili cihazları, kullanıcı cihazlarını veya cihaz grubu cihazlarını seçilen stratejiye ekleyin.

---

## API Belirteci (Token)

Öncelikle **Ayarlar → Belirteçler → Oluştur** bölümüne gitmeli ve gerekli izinlerle bir belirteç oluşturmalısınız: **Device, Audit Log, User, Group, Strategy, Address Book, Admin Role, Control Role**.

Oluşturulduktan sonra, bu belirteçleri karşılık gelen izinlerle eylemler gerçekleştirmek için **komut satırı** veya **Python CLI** aracılığıyla kullanabilirsiniz.

### Komut Satırından Belirteç ile Atama Yapma

RustDesk yürütülebilir dosyasını `--assign` parametresi ile kullanarak da atamalar yapabilirsiniz.  
Bu, kullanıcıları, stratejileri, adres defterlerini veya cihaz gruplarını doğrudan komut satırından bir cihaza atamayı sağlar.

**Example:**  

```bash
"C:\Program Files\RustDesk\rustdesk.exe" --assign --token <generatedtoken> --user_name <username>
```

Desteklenen Parametreler

| Parametre                               | Açıklama                                | RustDesk Server Pro | RustDesk İstemci |
| --------------------------------------- | --------------------------------------- | ------------------- | --------------- |
| `--user_name <username>`                | Cihaza bir kullanıcı atar             |                     |                 |
| `--strategy_name <strategyname>`        | Cihaza bir strateji atar         |                     |                 |
| `--address_book_name <addressbookname>` | Cihazı bir adres defterine atar        |                     |                 |
| `--address_book_tag <addressbooktag>`   | Adres defteri etiketiyle atar            |                     |                 |
| `--address_book_alias <alias>`          | Adres defteri takma adıyla atar          | 1.5.8               | 1.4.1           |
| `--address_book_password <password>`    | Adres defteri girdisi için parola belirler | 1.6.6               | 1.4.3           |
| `--address_book_note <note>`            | Adres defteri girdisi için not belirler     | 1.6.6               | 1.4.3           |
| `--device_group_name <devicegroupname>` | Cihazı bir cihaz grubuna atar         |                     |                 |
| `--note <note>`                         | Cihaza not ekler                  | 1.6.6               | 1.4.3           |
| `--device_username <device_username>`   | Cihaz kullanıcı adını belirler                 | 1.6.6               | 1.4.3           |
| `--device_name <device_name>`           | Cihaz adını belirler                     | 1.6.6               | 1.4.3           |
| [`--deploy`](/docs/tr/self-host/client-deployment/#explicit-deployment-for-new-devices) | Register a new device when **Require deployment for new devices** is enabled. Requires an API token with **Devices** permission set to **Read and write**. | 1.8.3 | 1.4.7 |

Windows'ta komut satırı varsayılan olarak çıktı vermez. Çıktı almak için lütfen `"C:\Program Files\RustDesk\rustdesk.exe" <arg1> <arg2> ... | more` veya `"C:\Program Files\RustDesk\rustdesk.exe" <arg1> <arg2> ... | Out-String` şeklinde çalıştırın, bkz. [burası](https://github.com/rustdesk/rustdesk/discussions/6377#discussioncomment-8094952).

### Python CLI Yönetim Araçları

#### Kullanıcı Yönetimi (`users.py`)

**Yardımı göster:**  
`./users.py -h`

**Kullanıcıları görüntüle:**  
`./users.py --url <url> --token <token> view [--name <username>] [--group_name <group_name>]`

**Filtreler:**  
- `--name`: username (fuzzy search)
- `--group_name`: user group (exact match)

**Example:**  
`./users.py --url https://example.com --token <token> view --group_name Default`

**Temel işlemler:**

- **Kullanıcıyı devre dışı bırak:**  
  `./users.py --url <url> --token <token> disable --name testuser`

- **Kullanıcıyı etkinleştir:**  
  `./users.py --url <url> --token <token> enable --name testuser`

- **Kullanıcıyı sil:**  
  `./users.py --url <url> --token <token> delete --name testuser`

**Kullanıcı oluşturma ve davet:**

- **Yeni kullanıcı oluştur:**  
  `./users.py --url <url> --token <token> new --name username --password 'password123' --group_name Default [--email user@example.com] [--note "note"]`
  
  Gerekli: `--name`, `--password`, `--group_name`  
  İsteğe bağlı: `--email`, `--note`

- **Invite user by email:**  
  `./users.py --url <url> --token <token> invite --email user@example.com --name username --group_name Default [--note "note"]`
  
  Gerekli: `--email`, `--name`, `--group_name`  
  İsteğe bağlı: `--note`

**2FA and security operations:**

- **Enable 2FA enforcement:**  
  `./users.py --url <url> --token <token> enable-2fa-enforce --name username --web-console-url <console_url>`
  
  Gerekli: `--web-console-url`

- **Disable 2FA enforcement:**  
  `./users.py --url <url> --token <token> disable-2fa-enforce --name username [--web-console-url <console_url>]`
  
  İsteğe bağlı: `--web-console-url`

- **Reset 2FA:**  
  `./users.py --url <url> --token <token> reset-2fa --name username`

- **Disable email verification:**  
  `./users.py --url <url> --token <token> disable-email-verification --name username`

- **Force logout:**  
  `./users.py --url <url> --token <token> force-logout --name username`

**Notes:**
- When operating on multiple users (matched by filters), you will be prompted for confirmation
- If no users match the filter, it will display "Found 0 users"

---

#### User Groups Management (`user-groups.py`)

**Yardımı göster:**  
`./user-groups.py -h`

**View user groups:**  
`./user-groups.py --url <url> --token <token> view [--name <group_name>]`

**Example:**  
`./user-groups.py --url https://example.com --token <token> view --name "Sales Team"`

**Group operations:**

- **Create user group:**  
  `./user-groups.py --url <url> --token <token> add --name "GroupName" [--note "description"] [--accessed-from '<json>'] [--access-to '<json>']`
  
  Example with access control:  
  `./user-groups.py --url <url> --token <token> add --name "Engineering" --accessed-from '[{"type":0,"name":"Managers"}]' --access-to '[{"type":1,"name":"DevServers"}]'`

- **Update user group:**  
  `./user-groups.py --url <url> --token <token> update --name "GroupName" [--new-name "NewName"] [--note "new note"] [--accessed-from '<json>'] [--access-to '<json>']`

- **Delete user group:**  
  `./user-groups.py --url <url> --token <token> delete --name "GroupName"`
  
  Supports comma-separated names: `--name "Group1,Group2,Group3"`

**User management in groups:**

- **View users in group:**  
  `./user-groups.py --url <url> --token <token> view-users [--name <group_name>] [--user-name <username>]`
  
  Filters:
  - `--name`: group name (exact match, optional)
  - `--user-name`: username (fuzzy search, optional)
  
  Example:  
  `./user-groups.py --url <url> --token <token> view-users --name Default --user-name john`

- **Add users to group:**  
  `./user-groups.py --url <url> --token <token> add-users --name "GroupName" --users "user1,user2,user3"`

**Access control parameters:**

- `--accessed-from`: JSON array defining who can access this user group
  - Type 0 = User Group (e.g., `[{"type":0,"name":"Admins"}]`)
  - Type 2 = User (e.g., `[{"type":2,"name":"john"}]`)

- `--access-to`: JSON array defining what this user group can access
  - Type 0 = User Group (e.g., `[{"type":0,"name":"Support"}]`)
  - Type 1 = Device Group (e.g., `[{"type":1,"name":"Servers"}]`)

**Permission requirements:**
- `view/add/update/delete/add-users` commands require **User Group Permission**
- `view-users` command requires **User Permission**

---

#### Admin Roles Management (`admin-roles.py`)

The token must belong to a full administrator and have **Admin Role** read or read/write permission. Commands that resolve user names or list role members also require **User** read permission.

**View roles:**

```bash
# List roles, optionally filtered by exact name or type
./admin-roles.py --url <url> --token <token> view [--name <role_name>] [--type global|individual|group]

# View one role by GUID
./admin-roles.py --url <url> --token <token> view --guid <role_guid>
```

**Create a role:**

```bash
# Global role
./admin-roles.py --url <url> --token <token> add \
  --name "Support Admin" --type global \
  --permissions "users.view,devices.view,audits.view" --note "Read-only support"

# Group-scoped role
./admin-roles.py --url <url> --token <token> add \
  --name "Support Scope" --type group \
  --permissions "users.view,devices.view,devices.enable_disable" \
  --user-groups "Support" --device-groups "Servers" --unassigned
```

The role type cannot be changed after creation. `--permissions` accepts comma-separated permission names, decimal IDs, or `0x`-prefixed IDs, and the formats can be mixed. For example, `users.view,513,0x0203` is equivalent to `257,513,515`. The server rejects permissions that are not valid for the selected role type.

The `view` command converts known permission IDs back to the names below. An ID unknown to the script is preserved as a number so permissions added by a newer server are not hidden.

| Area | Permissions | Valid role types |
| --- | --- | --- |
| Users | `users.view` (`257`); `users.create` (`259`); `users.invite` (`260`); `users.delete` (`261`); `users.enable_disable` (`262`); `users.edit_email` (`263`); `users.edit_password` (`264`); `users.edit_note` (`265`); `users.manage_2fa` (`266`); `users.force_logout` (`267`); `users.change_strategy` (`269`); `users.change_control_role` (`270`); `users.edit_display_name` (`271`) | global, group |
| Users | `users.change_group` (`268`) | global |
| Devices | `devices.view` (`513`) | global, group |
| Devices | `devices.enable_disable` (`515`); `devices.delete` (`516`); `devices.edit_info` (`517`); `devices.change_strategy` (`520`) | global, individual, group |
| Devices | `devices.assign_to_user` (`518`); `devices.change_group` (`519`) | global |
| User groups | `user_groups.view` (`769`); `user_groups.edit` (`770`) | global |
| Device groups | `device_groups.view` (`1025`); `device_groups.edit` (`1026`); `device_groups.change_strategy` (`1027`) | global |
| Audits | `audits.view` (`1281`); `audits.edit` (`1282`) | global, individual |
| Strategies | `strategies.view` (`1537`); `strategies.edit` (`1538`) | global |
| Custom clients | `custom_clients.view` (`1793`); `custom_clients.edit` (`1794`) | global |
| Control roles | `control_roles.view` (`2049`); `control_roles.edit` (`2050`) | global |

**Update or delete a role:**

```bash
./admin-roles.py --url <url> --token <token> update --name "Support Admin" \
  [--new-name "Helpdesk Admin"] [--note "new note"] [--permissions "users.view,devices.view"] \
  [--user-groups "Support"] [--device-groups "Servers"] [--unassigned|--no-unassigned]

./admin-roles.py --url <url> --token <token> delete --name "Support Admin"
```

Pass an empty value to clear `--note`, `--permissions`, `--user-groups`, or `--device-groups`, for example `--permissions ""`.

**Manage role members:**

```bash
./admin-roles.py --url <url> --token <token> view-users --name "Support Admin"
./admin-roles.py --url <url> --token <token> add-users --name "Support Admin" --users "user1,user2"
./admin-roles.py --url <url> --token <token> remove-users --name "Support Admin" --users "user1,user2"
```

Role targets and users can also be supplied by GUID. User names and GUIDs can be mixed in `--users`.

---

#### Control Roles Management (`control-roles.py`)

The token needs **Control Role** read or read/write permission. Commands that resolve user names or list role members also require **User** read permission.

**View roles:**

```bash
./control-roles.py --url <url> --token <token> view [--name <role_name>] [--status enabled|disabled]
./control-roles.py --url <url> --token <token> view --guid <role_guid>
```

**Create, update, delete, enable, or disable a role:**

```bash
./control-roles.py --url <url> --token <token> add --name "Contractors" [--note "Restricted access"]
./control-roles.py --url <url> --token <token> update --name "Contractors" [--new-name "Vendors"] [--note "new note"]
./control-roles.py --url <url> --token <token> delete --name "Contractors"
./control-roles.py --url <url> --token <token> enable --name "Contractors"
./control-roles.py --url <url> --token <token> disable --name "Contractors"
```

New roles created by this script do not include control permissions. Configure them in the web console before assigning users. Control-permission definitions are not managed or displayed by this script.

**Manage role members:**

```bash
./control-roles.py --url <url> --token <token> view-users --name "Contractors"
./control-roles.py --url <url> --token <token> assign-users --name "Contractors" --users "user1,user2"
./control-roles.py --url <url> --token <token> remove-users --users "user1,user2"
```

Role targets and users can also be supplied by GUID. `remove-users` clears each user's current control role, so it does not take `--name` or `--guid`. For the reserved `Default` role, `view-users` lists explicit assignments only; users without a control-role assignment also inherit `Default`. The reserved `Not Logged` role cannot be assigned to users, and reserved roles cannot be renamed, given a note, or deleted.

---

#### Device Groups Management (`device-groups.py`)

**Yardımı göster:**  
`./device-groups.py -h`

**View device groups:**  
`./device-groups.py --url <url> --token <token> view [--name <group_name>]`

**Example:**  
`./device-groups.py --url https://example.com --token <token> view`

**Group operations:**

- **Create device group:**  
  `./device-groups.py --url <url> --token <token> add --name "GroupName" [--note "description"] [--accessed-from '<json>']`
  
  Example:  
  `./device-groups.py --url <url> --token <token> add --name "Production" --accessed-from '[{"type":0,"name":"Admins"}]'`

- **Update device group:**  
  `./device-groups.py --url <url> --token <token> update --name "GroupName" [--new-name "NewName"] [--note "new note"] [--accessed-from '<json>']`

- **Delete device group:**  
  `./device-groups.py --url <url> --token <token> delete --name "GroupName"`
  
  Supports comma-separated names: `--name "Group1,Group2,Group3"`

**Device management in groups:**

- **View devices in group:**  
  `./device-groups.py --url <url> --token <token> view-devices [filters]`
  
  Available filters:
  - `--name`: device group name (exact match)
  - `--id`: device ID (fuzzy search)
  - `--device-name`: device name (fuzzy search)
  - `--user-name`: user name/owner (fuzzy search)
  - `--device-username`: logged-in username on device (fuzzy search)
  
  Examples:  
  ```bash
  # View all devices in a group
  ./device-groups.py --url <url> --token <token> view-devices --name Production
  
  # Search by device name
  ./device-groups.py --url <url> --token <token> view-devices --device-name server
  
  # Combine filters
  ./device-groups.py --url <url> --token <token> view-devices --name Production --user-name john
  ```

- **Add devices to group:**  
  `./device-groups.py --url <url> --token <token> add-devices --name "GroupName" --ids "deviceid1,deviceid2"`

- **Remove devices from group:**  
  `./device-groups.py --url <url> --token <token> remove-devices --name "GroupName" --ids "deviceid1,deviceid2"`

**Access control parameter:**

- `--accessed-from`: JSON array defining who can access this device group
  - Type 0 = User Group (e.g., `[{"type":0,"name":"Engineers"}]`)
  - Type 2 = User (e.g., `[{"type":2,"name":"admin"}]`)

**Permission requirements:**
- `view/add/update/delete/add-devices/remove-devices` commands require **Device Group Permission**
- `view-devices` command requires **Device Permission**

---

#### Devices Management (`devices.py`)

**Yardımı göster:**  
`./devices.py -h`

**View devices:**  
`./devices.py --url <url> --token <token> view [--id <device_id>] [--device_name <device_name>] [--user_name <user_name>] [--group_name <group_name>] [--device_group_name <device_group_name>] [--offline_days <days>]`

**Filtreler:**  
`--id`: device ID  
`--device_name`: device name  
`--user_name`: assigned user  
`--group_name`: user group  
`--device_group_name`: device group  
`--offline_days`: days offline

**Example:**  
`./devices.py --url https://example.com --token <token> view --user_name mike`

**Operations:**  
view can be replaced with `enable`, `disable`, `delete`, or `assign`.

**Example (assign device):**  
`./devices.py --url https://example.com --token <token> assign --device_name PC01 --assign_to user_name=mike`

---

#### Address Book Management (`ab.py`)

**Yardımı göster:**  
`./ab.py -h`

**View shared address books:**  
`./ab.py --url <url> --token <token> view-ab [--ab-name <address_book_name>]`

**Get personal address book GUID:**  
`./ab.py --url <url> --token <token> get-personal-ab`

**Add a shared address book:**  
`./ab.py --url <url> --token <token> add-ab --ab-name <name> [--note <note>] [--password <password>]`

**Update or delete a shared address book:**  
`./ab.py --url <url> --token <token> update-ab --ab-guid <guid> [--ab-update-name <new_name>] [--note <note>]`  
`./ab.py --url <url> --token <token> delete-ab --ab-guid <guid>`

**View peers in an address book:**  
`./ab.py --url <url> --token <token> view-peer --ab-guid <guid> [--peer-id <peer_id>] [--alias <alias>]`

**Add, update, or delete a peer:**  
`./ab.py --url <url> --token <token> add-peer --ab-guid <guid> --peer-id <peer_id> [--alias <alias>] [--note <note>] [--tags tag1,tag2]`  
`./ab.py --url <url> --token <token> update-peer --ab-guid <guid> --peer-id <peer_id> [--alias <alias>] [--note <note>] [--tags tag1,tag2]`  
`./ab.py --url <url> --token <token> delete-peer --ab-guid <guid> --peer-id <peer_id>`

**Tags management:**  
`./ab.py --url <url> --token <token> view-tag --ab-guid <guid>`  
`./ab.py --url <url> --token <token> add-tag --ab-guid <guid> --tag-name <name> [--tag-color 0xFF00FF00]`  
`./ab.py --url <url> --token <token> update-tag --ab-guid <guid> --tag-name <name> --tag-color 0xFFFF0000`  
`./ab.py --url <url> --token <token> delete-tag --ab-guid <guid> --tag-name <name>`

**Access rules management:**  
`./ab.py --url <url> --token <token> view-rule --ab-guid <guid>`  
`./ab.py --url <url> --token <token> add-rule --ab-guid <guid> [--rule-type user|group|everyone] [--rule-user <user>] [--rule-group <group>] --rule-permission ro|rw|full`  
`./ab.py --url <url> --token <token> update-rule --rule-guid <rule_guid> --rule-permission rw`  
`./ab.py --url <url> --token <token> delete-rule --rule-guid <rule_guid>`

**Example (add read-only rule for user "mike"):**  
`./ab.py --url https://example.com --token <token> add-rule --ab-guid <guid> --rule-user mike --rule-permission ro`

---

#### Strategies Management (`strategies.py`)

**Yardımı göster:**  
`./strategies.py -h`

**List all strategies:**  
`./strategies.py --url <url> --token <token> list`

**View a specific strategy:**  
```bash
# By name
./strategies.py --url <url> --token <token> view --name "Default"

# By GUID
./strategies.py --url <url> --token <token> view --guid "01983006-fcca-7c12-9a91-b1df483c6073"
```

**Enable or disable a strategy:**  
```bash
./strategies.py --url <url> --token <token> enable --name "StrategyName"
./strategies.py --url <url> --token <token> disable --name "StrategyName"
```

**Assign strategy to devices, users, or device groups:**  
```bash
# Assign to devices (by device ID)
./strategies.py --url <url> --token <token> assign --name "Default" --peers "1849118658,1337348840"

# Assign to users (by username)
./strategies.py --url <url> --token <token> assign --name "Default" --users "admin,user1"

# Assign to device groups (by group name)
./strategies.py --url <url> --token <token> assign --name "Default" --device-groups "device_group1,Production"

# Mixed assignment
./strategies.py --url <url> --token <token> assign \
  --name "Default" \
  --peers "1849118658" \
  --users "admin" \
  --device-groups "device_group1"
```

**Unassign strategy:**  
```bash
# Unassign from devices
./strategies.py --url <url> --token <token> unassign --peers "1849118658,1337348840"

# Unassign from users
./strategies.py --url <url> --token <token> unassign --users "admin"

# Unassign from device groups
./strategies.py --url <url> --token <token> unassign --device-groups "device_group1"
```

**Notes:**
- The script supports both names and GUIDs for users and device groups
- Device IDs are automatically converted to GUIDs
- All assign/unassign operations can target multiple resources at once

**Permission requirements:**
- `list/view/enable/disable/assign/unassign` commands require **Strategy Permission**
- `--peers` requires **Device Permission:r** (for ID to GUID lookup)
- `--users` requires **User Permission:r** (for username to GUID lookup)
- `--device-groups` requires **Device Group Permission:r** (for name to GUID lookup)

---

#### Audits (`audits.py`)

**Yardımı göster:**  
`./audits.py -h`

**View connection audits:**  
`./audits.py --url <url> --token <token> view-conn [--remote <peer_id>] [--conn-type <type>] [--page-size <n>] [--current <n>] [--created-at <"YYYY-MM-DD HH:MM:SS">] [--days-ago <n>]`

**View file audits:**  
`./audits.py --url <url> --token <token> view-file [--remote <peer_id>] [--page-size <n>] [--current <n>] [--created-at <"YYYY-MM-DD HH:MM:SS">] [--days-ago <n>]`

**View alarm audits:**  
`./audits.py --url <url> --token <token> view-alarm [--device <device_id>] [--page-size <n>] [--current <n>] [--created-at <"YYYY-MM-DD HH:MM:SS">] [--days-ago <n>]`

**View console audits:**  
`./audits.py --url <url> --token <token> view-console [--operator <username>] [--page-size <n>] [--current <n>] [--created-at <"YYYY-MM-DD HH:MM:SS">] [--days-ago <n>]`

**Filtreler:**  
`--remote`: Peer ID (for connection or file audits)  
`--conn-type`: 0=Remote Desktop, 1=File Transfer, 2=Port Transfer, 3=View Camera, 4=Terminal  
`--device`: Device ID (for alarm audits)  
`--operator`: Operator username (for console audits)  
`--created-at`: Local time filter, e.g., "2025-09-16 14:15:57"  
`--days-ago`: Filter records newer than given days ago  
`--page-size` / `--current`: Pagination

**Example:**  
`./audits.py --url https://example.com --token <token> view-conn --remote 123456789 --days-ago 7`


## Bir cihazı arama
1. Cihazlar'a gidin.
2. Cihaz Adı Arama Alanına adı yazın ve `Sorgula` (Query) seçeneğine tıklayın veya <kbd>Enter</kbd> tuşuna basın.
3. Joker karakter kullanmak için arama teriminin başına, sonuna veya her iki tarafına `%` ekleyin.
