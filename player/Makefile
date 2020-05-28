CC = clang
CFLAG = -std=c11 -Wall -Wextra -Werror -Wpedantic -I./inc

FRM_DIR=./resource/Frameworks

SDL2 = -I ${FRM_DIR}/SDL2.framework/Versions/A/Header \
	-F ${FRM_DIR} -framework SDL2
SDL2_MIX = -I ${FRM_DIR}/SDL2_mixer.framework/Versions/A/Headers \
	-F ${FRM_DIR}/ -framework SDL2_mixer

BINARY = mupmp3

CFILES = src/*.c

all: uninstall ${BINARY}

${BINARY}:
	@${CC} ${CFLAG} ${CFILES} -o ${BINARY} ${SDL2} ${SDL2_MIX} -rpath ${FRM_DIR}
uninstall:
	@rm -rf ${BINARY}
clean:
	@rm -rf *.o
reinstall: all
