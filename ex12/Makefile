
CC					:= gcc

RM					:= rm -rf

LDFLAGS			+= -Llib

CFLAGS			+= -Iinclude

SRCS				:= $(wildcard src/*.c)

OBJS				:= $(SRCS:.c=.o)

NAME				:= halloc_test

all:				$(NAME)

$(NAME):		$(OBJS)
						$(CC) -o $(NAME) $(OBJS) $(LDFLAGS)

clean:
						$(RM) $(OBJS)

fclean: 		clean
						$(RM) $(NAME)

re: 				fclean all

test:				re
						@(./$(NAME) && echo "Test success" || echo "Test Fails")
