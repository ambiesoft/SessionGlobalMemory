# SessionGlobalMemory
A C++ class to access win32 Shared Memory 

# How to use
1. include *SessionGlobalMemory.h* in you project.
2. Define a variable as follows.
```
CSessionGlobalMemory<Data> sgData("sgData");
```
This creates a Shared Memory named "sgData" and Mutex for exclusive access named "sgData_Mutex". Other processes can create same name object that can access this *Data*. *Data* must not include a pointer since it is invalid between processes. Offcourse basic types like *int* or *HWND* can be used as type.

