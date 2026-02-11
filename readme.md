git clone https://github.com/SanReg/automation3.git
cd automation3

nano .env
Paste or type the variables (example below).
Save: Ctrl+O, press Enter.
Exit: Ctrl+X.
In many terminals paste via right‑click or Shift+Insert.

docker build -t automation3

docker run -d \
  --name automation3 \
  --env-file .env \
  -p 3000:3000 \
  -v $(pwd)/temp:/usr/src/app/temp \
  --restart unless-stopped \
  automation3


  After update;
  git pull
  git build -t automation3 .
