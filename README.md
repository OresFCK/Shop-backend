Potrzebne do projektu:

PostreSQL
PHP w wersji 8+ (zainstaluj najnowsza)
Composer
Symfony (tutaj tez najlepiej najnowsza)
Symfony cli (nie jest wymagane ale jest rekomendowane żeby ułatwić sobie prace)

(tutaj przy instalacji symfony i php polecam po prostu isc z dokumentacja albo jakims szybkim poradnikiem z yt nic trudnego robisz wszystko krok po kroku)

Kroki potrzebne do "odpalenia"

stworz sobie .env.local na podstawie .env
composer install
php bin/console doctrine:create:database
php bin/console doctrine:migration:migrate
(w przyszłośosci bedzie potrzebne jeszcze data:fixtures:load ale na razie tego nie robimy bo nie potrzebujemy jeszcze danych testowych)

No i finalnie stawawiamy web-server czyli włączamy backend

jesli korzystasz z symfony cli wystarczy 

symfony server:start 

jesli nie to wtedy wpisujesz 

php -S localhost:8000 -t public

w tym momencie pod adresem localhost:8000 zobaczysz bazowy widok symfony (moga pojawic sie bledy w konsoli ale na tym etapie je zignoruj po prostu symfony bedzie probowac 
wygenerowac widok ktorego nie ma, z tego co wiem tego warninga nie da sie obejsc w zaden sposob wiec tymczasoow musi zostac)