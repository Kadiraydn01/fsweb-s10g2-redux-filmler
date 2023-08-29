# Redux React Modül Projesi: Filmler

Bugün, redux felsefesini gördünüz ve redux ile çalışmayı (store oluşturmayı, action oluşturucu fonksiyonları, bir actionu dispatch etmeyi, reducer yaratmayı ve store içerisindeki verileri sayfada görüntülemeyi) öğrendiniz.

## Giriş

Bu projede, küçük bir film veritabanı içeren bir web uygulamasında çalışacak, iki farklı reducer ile işlem yapacaksınız. Hem mevcut tüm state ve action oluşturucuları kullanacak, hem de sıfırdan reducer/redux pairing'leri oluşturacaksınız.

![Film DB örneği](./proje-demo.mov)

**_Görevlerinizi tek tek tamamladığınızdan ve ilerlemeden önce her bir görevi test ettiğinizden emin olun.._**

## Talimatlar

- **Film Ekleme Action'ı:**

  - [ ] Bir filmin eklenmesini tetikleyen componenti bulun ve `addMovie` action'ını bağlayın.
  - [ ] `addMovie`'yi çağırmak için gerekli event handlerı oluşturun ve bağlayın.
  - [ ] Yeni bir film eklerken `id` değeri olarak `Date.now()` kullanın.
  - [ ] Film eklendikten sonra filmler sayfasına yönlendirmek için `push('/movies/')` komutunu ekleyin.

#### Favoriler reducerı oluşturun

> _Tebrikler 👏 Artık film reducerı tamamlandığına göre, favori film özelliği için sıfırdan bir reducer oluşturabiliriz. Reducerları birleştirme (`combineReducers`) konusunda çalışacağız._

- [ ] Favoriler özelliği için bir **reducer dosyası** oluşturun. Bu dosyada kullanacağınız `initialState` objesine aşağıdaki değerlerini ekleyin:

  - `favorites { Film[] }`: Film nesnesini içeren bir dizi (başlangıç değeri `[]`).
  - `displayFavorites { Boolean }`: Uygulamada favorilerin göster/gizle değerini tutan bir boolean (başlangıç değeri `false`).

- [ ] `switch` deyimine `default` case'ini ekleyin.

- [ ] Yeni reducerınızı `./reducers/index.js` dosyasına import edin.

- [ ] `reducers/index.js`'de hem `moviesReducer`'ı hem de favori reducer'ı redux'a bağlamak için `combineReducers` metodunu kullanın.

- [ ] **Film işlevlerinizin artık çalışmadığına dikkat edin. Neden?** &nbsp;`movieReducer`a bağlı componentlerin tekrar çalışmasını sağlamak için gerekli değişiklikleri yapın.

- [ ] Store içerisinden `favorites` değerini `FavoriteMovieList` componentine bağlayın ve test edin.

- [ ] `DisplayFavorites` değerini store içerisinden çekerek `Movie` ve `AppHeader` componentinde ilgili yerlerde kullanın.

#### Favoriler eylemleri ekleyin

> _Şimdi, uygulamanın geri kalanını kendi başınıza oluşturacaksınız. Bunu yapabilirsiniz!_

1. Aşağıdaki eylemler için action generator'lar hazır. Siz de reducer case'leri ve event handler kodlarını ekleyin:

- `toggleFavorites`: `displayFavorites` state değerini `true` ve `false` olarak değiştirir. `displayFavorites` `false` olduğunda, favori filmler componenti uygulamada görünmez.

- `addFavorite`: Favoriler listesine yeni bir film nesnesi ekler.
- `removeFavorite`: Gönderilen bir id ile bir film Nesnesini favoriler listesinden kaldırır.

### Esnek Görevler

- Favoriler görüntülenmiyorsa, kullanıcının bir öğeyi favorilere eklemesine izin vermemek mantıklıdır. Ekleme, favori düğmesinin SADECE displayFavorite true ise görüntülenmesi anlamına gelir.

- Şu anda, aynı filmi birden çok kez favorilerinize ekleyebilirsiniz. Yalnızca listede olmayan filmleri favorilere eklenebilir hale getirmek için AddFavorite eylemini güncelleyin.

- Eğer film ana filmler listesinden silinirse, favorilere ekliyse ordan da silinmelidir, kodunuzu buna göre güncelleyin.

- İçeriklerinizi stilleyin ❤️

Tebrikler!
&nbsp;
Projeyi başarıyla tamamladın 👏👏👏
