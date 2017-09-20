### Installation on Mac OSX
```
git clone https://github.com/v00d00sec/telegram-cli.git && cd telegram-cli
brew install libconfig readline lua python libevent jansson
export CFLAGS="-I/usr/local/include -I/usr/local/Cellar/readline/7.0.3_1/include"
export CPPFLAGS="-I/usr/local/opt/openssl/include"
export LDFLAGS="-L/usr/local/opt/openssl/lib -L/usr/local/lib -L/usr/local/Cellar/readline/7.0.3_1/lib"
./configure --with-openssl=/usr/local/opt/openssl && make
```
### Notes:
- If you are getting libreadline errors during `./configure`, run `brew list readline` and change the path in the export flags above accordingly.
- Commented `lua-tg.c` lines 664-666 in order to compile successfully.
- Forked for future use.
- All credits to author: Vitaly Valtman
