Pada Bagian `application/config/config.php`:

```php
// application/config/config.php

$config['composer_autoload'] = FALSE;

// ubah menjadi
$config['composer_autoload'] = 'vendor/autoload.php';
```

Kemudian ketikkan di Terminal:

```bash
composer require jenssegers/blade
```

Tambahkan `view` di `application/config/autoload.php`:

```php
// application/config/autoload.php

$autoload['helper'] = array('view');
```

Contoh cara penggunaan:

```php
// controller

$data = $this->db->get('santri')->result();

return view('index', array(
	'data' => $data
));
```

Lalu pada folder `views`, gunakan ekstensi `blade.php` seperti `index.blade.php`

# Sumber

<https://medium.com/easyread/menggunakan-blade-template-engine-pada-codeigniter-369b2eea024c>