keeperbot

admin:@best_boy

Installation

# Tested on Ubuntu 14.04, for other OSs check out https://github.com/mrjon1/keeperbot
sudo apt-get install libreadline-dev libconfig-dev libssl-dev lua5.2 liblua5.2-dev libevent-dev make unzip git redis-server g++ libjansson-dev libpython-dev expat libexpat1-dev
# After those dependencies, lets install the bot
cd $HOME
git clone https://github.com/mrjon1/keeperbot.git
cd telegram-bot
./launch.sh install
./launch.sh # Will ask you for a phone number & confirmation code.
Enable more plugins

See the plugins list with !plugins command.

Enable a disabled plugin by !plugins enable [name].

Disable an enabled plugin by !plugins disable [name].

Those commands require a privileged user, privileged users are defined inside data/config.lua (generated by the bot), stop the bot and edit if necessary.

Run it as a daemon

If your Linux/Unix comes with upstart you can run the bot by this way

$ sed -i "s/yourusername/$(whoami)/g" etc/telegram.conf
$ sed -i "s_telegrambotpath_$(pwd)_g" etc/telegram.conf
$ sudo cp etc/telegram.conf /etc/init/
$ sudo start telegram # To start it
$ sudo stop telegram # To stop it
Contact me
@best_boy
