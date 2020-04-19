### Get the compiler(Emscripten)
Follow the instruction given in their [website](https://emscripten.org/docs/getting_started/downloads.html) and install the compiler. After completing the installation, you will be able to access the command ```emcc``` from your terminal if everything goes right.

### Write your C Program
We have included one simple Hello World program here named as ```helloworld.c```
```
#include <stdio.h>

int main() {
    printf("Hello World from C\n");
    return 0;
}
```

### Compile your program using Emscripten
```
emcc helloworld.c -o helloworld
```
Once done you will be able to see two more new files called ```helloworld.js``` and ```helloworld.wasm```.

### Connect the compiled files with your Webpage
This is much more easier than you can think of. Simple add the ```helloworld.js``` file into your ```html``` file. 
```
<script src="helloworld.js"></script>
```

### Need a server to run
If you use your file directory ```file://``` to see the html file, it won't work. You need a server which can be very made usinh ```http-server``` and boom, once you open up your webpage, you will see your C program is showing output into your browser console.
