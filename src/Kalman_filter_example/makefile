OBJS = main.o tracking.o kalman_filter.o 
CC = g++
DEBUG = -g
CFLAGS = -Wall -c $(DEBUG)
LFLAGS = -Wall $(DEBUG)

monitor : $(OBJS)
	$(CC) $(LFLAGS) $(OBJS) -o monitor

main.o : main.cpp measurement_package.h tracking.h
	$(CC) $(CFLAGS) main.cpp

tracking.o : tracking.cpp tracking.h kalman_filter.h
	$(CC) $(CFLAGS) tracking.cpp

kalman_filter.o : kalman_filter.cpp kalman_filter.h
	$(CC) $(CFLAGS) kalman_filter.cpp

clean:
	\rm *.o *~ monitor 