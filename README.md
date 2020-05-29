
git clone https://github.com/YauhenRanko/test_DE
cd quickstart/python

Установите виртуальное окружение и активируйте

python -m venv env
source venv/bin/activate

Установите зависимости
pip install -r requirements.txt

Поолучите ключи подключите API GoogleDrive и GoogleSheets на https://console.developers.google.com/
Скачайте файл в формате JSON (переменная JSON_KEY_GOOGLE_FILE)


Получите и введите ключи API на https://plaid.com/eu/, получите логин и пароль для тестовой работы 
PLAID_CLIENT_ID='CLIENT_ID' \
PLAID_SECRET='SECRET' \
PLAID_PUBLIC_KEY='PUBLIC_KEY' \
PLAID_ENV='sandbox' \
PLAID_PRODUCTS='transactions' \
PLAID_COUNTRY_CODES='US' \
python server.py

# Go to http://localhost:5000

Войдите по логину и паролю и выберите банк 
Запросите транзакции за период Transactions /transactions/get 
Период можно менять в роуте @app.route('/transactions', methods=['GET']) в datetime.timedelta(ДНЕЙ НАЗАД) выберите сколько дней необходимо для анализа

Необработанные данные попадут на первый лист таблицы





