
### Why

- Non-members have no way to download game PGN's
- Free users have to download a file (which is a pain)
- 100% of the time I just copy/paste it into lichess' import tool

### Installation

*OSX*

```
$ pip install -r requirements.txt
$ brew install phantomjs
```

### Usage

```
$ ./chesscom-pgn 1446963708
[Event "Live Chess"]
[Site "Chess.com"]
[Date "2016.02.02"]
[White "shrekdavid"]
[Black "Hikaru"]
[WhiteElo "2376"]
[BlackElo "2829"]
[TimeControl "3|2"]
[Termination "Hikaru won by resignation"]

1.e4 b6 2.d4 Bb7 3.Bd3 e6 4.Qe2 d5 5.Nf3 Nf6 6.e5 Nfd7 7.c3 c5 8.a3 Be7 9.b4 a5 10.b5 a4 11.O-O c4 12.Bc2 Ra5 13.Ra2 Rxb5 14.Nbd2 Ra5 15.Ne1 h5 16.f4 g6 17.g3 Nc6 18.Ng2 b5 19.Ne3 Nb6 20.h3 Bc8 21.g4 hxg4 22.hxg4 Kd7 23.Nf3 Qg8 24.Kg2 Kc7 25.Bb2 Bd7 26.Raa1 Ra8 27.Rh1 Qg7 28.g5 Rxh1 29.Rxh1 Qf8 30.Ra1 Na5 31.Ng4 Nb3 32.Ra2 Qg7 33.Nh4 Rh8 34.Kg3 Bc6 35.Qf2 Qh7 36.Nh6 Bf8 37.Nf3 Bxh6 38.gxh6 Qxh6 39.Ng5 Qh4+ 40.Kf3 Qxf2+ 41.Kxf2 Rh2+
```

```
$ ./chesscom-pgn 1446963708 --lichess
http://en.lichess.org/4mzSY6qI
```

Or better yet.

```
# alias chrome="open -a \"Google Chrome\""
$ chrome $(./chesscom-pgn 1446963708 --lichess)
```

### Caveats

Currently no way to scrape the pgn's `[Result]` header.