# Tempmails
api for tempmails.cc site for generate temporary email addresses for secure and anonymous communication
# main
```cpp
#include "Tempmails.h"
#include <iostream>

int main() {
   Tempmails api;
    auto email = api.generate_email().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    email.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
