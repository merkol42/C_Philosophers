NAME	:= philo

CC		:= gcc
SRC_DIR	:= src
SRC		:= $(wildcard $(SRC_DIR)/*.c)

OBJ_DIR	:= obj
OBJ		:= $(SRC:$(SRC_DIR)/%.c=$(OBJ_DIR)/%.o)

INCLUDE	:= -I./include
CFLAGS	:= -Wall -Wextra -Werror $(INCLUDE)

all: $(NAME)

$(NAME): $(OBJ_DIR) $(OBJ)
	$(CC) $(CFLAGS) $(OBJ) -o $(NAME)

$(OBJ_DIR):
	@mkdir -p $(OBJ_DIR)

$(OBJ_DIR)/%.o: $(SRC_DIR)/%.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJ)

fclean: clean
	rm -rf $(NAME) $(OBJ_DIR)

re:	clean all