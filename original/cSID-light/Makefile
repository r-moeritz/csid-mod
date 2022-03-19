
all: csid-light.c # playlist
	gcc csid-light.c -s -o csidl `sdl-config --cflags --libs` -lm # -lSDL
#	i686-w64-mingw32-gcc  csid-light.c  -s  -o csidl.exe  -Wl,-subsystem,console -lmingw32 -lmingwex -mwindows -lSDLmain -lSDL  -I/usr/local/sdlmingw/include  -L/usr/local/sdlmingw/lib

probe: csidl playlist.txt
	./csidl playlist.txt - - 125

install:
	-cp csidl /usr/local/bin
	-cp csida /usr/local/bin

playlist:
	touch playlist.txt
	ls music/*.sid > playlist.txt

clean:
	rm -f csidl csidl.exe csidl-win.o # playlist.txt

uninstall:
	rm -f /usr/local/bin/csidl /usr/local/bin/csida

purge: clean uninstall