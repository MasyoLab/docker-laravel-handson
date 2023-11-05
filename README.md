# docker-laravel-handson
## 参考
- [課金が怖いのでサーバー部分をDockerコンテナで代用してみました](https://cacapon.hatenablog.com/entry/2021/06/25/122420)
- [最強のLaravel開発環境をDockerを使って構築する](https://qiita.com/ucan-lab/items/5fc1281cd8076c8ac9f4)
- [【超入門】20分でLaravel開発環境を爆速構築するDockerハンズオン](https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4)

## インストール用のコマンド
```
docker compose exec app bash
chmod -R 777 storage bootstrap/cache
composer install
cp .env.example .env
php artisan key:generate
php artisan storage:link
exit
docker compose down
```

## 起動用のコマンド
```
docker compose build
docker compose up -d
```

[http://localhost:8080/](http://localhost:8080/)
