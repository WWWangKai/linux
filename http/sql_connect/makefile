.PHONY:all
all:select_cgi insert_cgi delete_cgi find_cgi

select_cgi:select_cgi.cpp sql_api.cpp
	g++ -o $@ $^ -I/home/http/sql_connect/include -L/home/http/sql_connect/lib -lmysqlclient 


insert_cgi:insert_cgi.cpp sql_api.cpp
	g++ -o $@ $^ -I/home/http/sql_connect/include -L/home/http/sql_connect/lib -lmysqlclient

delete_cgi:delete_cgi.cpp sql_api.cpp
	g++ -o $@ $^ -I/home/http/sql_connect/include -L/home/http/sql_connect/lib -lmysqlclient


find_cgi:find_cgi.cpp sql_api.cpp
	g++ -o $@ $^ -I/home/http/sql_connect/include -L/home/http/sql_connect/lib -lmysqlclient

.PHONY:output
output:
	cp insert_cgi /home/http/wwwroot/cgi_bin
	cp select_cgi /home/http/wwwroot/cgi_bin
	cp delete_cgi /home/http/wwwroot/cgi_bin
	cp find_cgi   /home/http/wwwroot/cgi_bin

.PHONY:clean
clean:
	rm -f select_cgi insert_cgi delete_cgi find_cgi
