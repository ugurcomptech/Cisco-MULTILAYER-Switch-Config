# Cisco MULTILAYER Switch Config


Multilayer switch (çok katmanlı anahtar) veya Layer 3 switch olarak adlandırılan bu ağ cihazı, ağ trafiğini hem Layer 2 (veri bağlantı katmanı) hem de Layer 3 (ağ katmanı) seviyelerinde yönlendirebilen bir ağ anahtar türüdür. Geleneksel ağ anahtarları (Layer 2 anahtarları), sadece MAC adreslerine dayalı olarak paketleri yönlendirebilirken, multilayer switchler aynı zamanda IP adreslerini kullanarak paketleri yönlendirebilir. Bu, daha karmaşık ağ yapıları oluşturmanıza ve daha fazla ağ segmentasyonu sağlamanıza olanak tanır.

Multilayer switchlerin temel görevleri şunlar olabilir:

VLAN Yönetimi: Farklı VLAN'lar arasında iletişimi kolaylaştırır. VLAN'lar, ağı mantıksal olarak böler ve ağdaki cihazların trafiği sınırlı bir VLAN içinde kalır.

Yönlendirme: Layer 3 özelliği sayesinde, IP tabanlı iletişimi sağlar. Ağdaki farklı IP alt ağlar arasında yönlendirme yapabilir.

Hızlandırılmış İşlem: Layer 3 switchler, yüksek hızlı paket işleme yetenekleri ile büyük veri trafiğini hızlandırabilirler.

Ağ Güvenliği: Multilayer switchler, ağ güvenliği için Access Control Lists (ACLs) gibi özellikleri destekler.

VLAN (Virtual Local Area Network) ise fiziksel bir ağı mantıksal olarak birden fazla sanal ağa bölmek için kullanılan bir teknolojidir. VLAN'lar, ağdaki farklı kullanıcı gruplarını veya cihazları izole etmek, ağ trafiğini düzenlemek ve ağ performansını artırmak için kullanılır.

VLAN'ların temel özellikleri şunlardır:

İzolasyon: VLAN'lar farklı kullanıcı gruplarını birbirinden izole edebilir, böylece bir VLAN içindeki cihazlar diğer VLAN'larla doğrudan iletişim kuramaz.

Yönetim Kolaylığı: Ağ yöneticileri, VLAN'ları fiziksel yerine mantıksal olarak düzenleyebilirler. Bu, ağ yönetimini daha etkili hale getirir.

Güvenlik: VLAN'lar ağ güvenliğini artırabilir, çünkü trafiği izole edebilir ve erişimi sınırlayabilirler.

Trafik Yönetimi: VLAN'lar, ağ trafiğini daha iyi düzenlemek için kullanılabilir. Örneğin, farklı işlevlere sahip cihazlar arasında trafiği ayırabilirsiniz.

Multilayer switchler, VLAN'ların yönetimini destekler ve farklı VLAN'lar arasında iletişimi kolaylaştırır. Bu, ağdaki veri akışını daha etkili hale getirir ve ağ yönetimini daha esnek kılar.



## Şimdi Yapılandırmalara geçelim:

### Multilayer Switch 1'e bağlı olan yapılandırmalar

### 2960 Switch1 (Vlan10)

```
Switch>en
Switch#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#vlan 10
Switch(config-vlan)#int range fa0/2
Switch(config-if-range)#switchport access vlan 10
Switch(config-if-range)#
```

### 2960 Switch2 (Vlan20)

```
Switch>en
Switch#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#vlan 20
Switch(config-vlan)#int range fa0/1
Switch(config-if-range)#switchport access vlan 20
Switch(config-if-range)#
```

### 2960 Switch3 (Vlan30)

```
Switch>en
Switch#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#vlan 30
Switch(config-vlan)#int range fa0/3
Switch(config-if-range)#switchport access vlan 30
Switch(config-if-range)#
```

### 2960 Switch3 (Vlan40)

```
Switch>en
Switch#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#vlan 40
Switch(config-vlan)#int range fa0/3
Switch(config-if-range)#switchport access vlan 40
Switch(config-if-range)#
```


