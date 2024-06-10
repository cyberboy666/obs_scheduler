# obs_schedular

_a simple webserver for scheduling obs broadcasts from m3u8 playlists_

this app uses __pythons__ _flask_ to server a web interface for scheduling __obs__ broadcasts using websockets.

you can set a `start_time`, `end_time` and `path to playlist file` - then provided obs is running and websockets are enabled at start time obs will load the playlist and start streaming it (on a loop) until the given end time

a _program times_ list is also generated with starting times of each video in the playlist

![image](https://github.com/cyberboy666/obs_scheduler/assets/12017938/63738f8c-d476-4e42-8a20-309b04853ec8)

_NOTE: This project was quickly put together to explore diy automated broadcasting for [subcarrier.tv](https://subcarrier.tv) - it is shared only to inspire / encourage others_

### how to run

- install python3 on your computer (i think you may need 3.9 or higher ?)
- clone this repo `git clone git@github.com:cyberboy666/obs_scheduler.git` and then `cd obs_scheduler` into the folder
- install dependancies: `pip3 install -r requirements.txt`
- open OBS and enable web-sockets (tools -> websocket server settings -> enable websocket server) and set `port:4444` and password `your_password` - or update `obs_scheduler.py` with port/password used here
- run the program: `python3 obs_scheduler.py `
- go to http://localhost:5000 to veiw the interface
