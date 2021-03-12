# login-with-username-and-passwor-in-laravel
login with username and passwor in laravel

+ Vảo file views/auth/login.blade.php sửa phàn input email thành input name
Cũ
```php
<input id="email" type="email" class="form-control @error('email') is-invalid @enderror" name="email" value="{{ old('email') }}" required autocomplete="email" autofocus>
@error('email')
    <span class="invalid-feedback" role="alert">
        <strong>{{ $message }}</strong>
    </span>
@enderror
```
Mới
```php
<input id="name" type="name" class="form-control @error('name') is-invalid @enderror" name="name" value="{{ old('name') }}" required  autofocus>
   
@error('name')
    <span class="invalid-feedback" role="alert">
        <strong>{{ $message }}</strong>
    </span>
@enderror
```


+ Vào file App\Http\Controller\Auth\LoginController.php và thêm hàm sau 
```php
    public function username()
    {
        return 'name';
    }
```
