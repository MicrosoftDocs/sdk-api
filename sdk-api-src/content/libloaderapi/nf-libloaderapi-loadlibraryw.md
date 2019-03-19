---
UID: NF:libloaderapi.LoadLibraryW
title: LoadLibraryW function (libloaderapi.h)
author: windows-sdk-content
description: Loads the specified module into the address space of the calling process.
old-location: base\loadlibrary.htm
tech.root: Dlls
ms.assetid: d936b4dd-058c-48e1-834b-b47ef6d8ef65
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LoadLibrary, LoadLibrary function, LoadLibraryA, LoadLibraryW, _win32_loadlibrary, base.loadlibrary, libloaderapi/LoadLibrary, libloaderapi/LoadLibraryA, libloaderapi/LoadLibraryW, winbase/LoadLibrary, winbase/LoadLibraryA, winbase/LoadLibraryW
ms.topic: function
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadLibraryW (Unicode) and LoadLibraryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - LoadLibrary
 - LoadLibraryA
 - LoadLibraryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LoadLibraryW function


## -description


Loads the specified  module into the address space of the calling process. The specified 
    module may cause other modules to be loaded.

For additional load options, use the 
    <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a> function.


## -parameters




### -param lpLibFileName [in]

The name of the module. This can be either a library module (a .dll file) or an executable 
       module (an .exe file). The name specified is the file name of the module and is not related to the 
       name stored in the library module itself, as specified by the <b>LIBRARY</b> keyword in 
       the module-definition (.def) file.

If the string specifies a full path, the function searches only that path for the module.

If the string specifies a relative path or a module name without a path, the function uses a standard search 
       strategy to find the module; for more information, see the Remarks.

If the function cannot find the  module, the function fails. When specifying a path, be sure to use 
       backslashes (\), not forward slashes (/). For more information about paths, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File or Directory</a>.

If the string specifies a module name without a path and the file name extension is omitted, the function 
       appends the default library extension .dll to the module name. To prevent the function from appending 
       .dll to the module name, include a trailing point character (.) in the module name string.


## -returns



If the function succeeds, the return value is a handle to the module.

If the function fails, the return value is NULL. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To enable or disable error messages displayed by the loader during DLL loads, use the 
    <a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a> function.

<b>LoadLibrary</b> can be used to load a library module into 
    the address space of the process and return a handle that can be used in 
    <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to get the address of a DLL function. 
    <b>LoadLibrary</b> can also be used to load other executable 
    modules. For example, the function can specify an .exe file to get a handle that can be used in 
    <a href="https://msdn.microsoft.com/en-us/library/ms648042(v=VS.85).aspx">FindResource</a> or 
    <a href="https://msdn.microsoft.com/en-us/library/ms648046(v=VS.85).aspx">LoadResource</a>. However, do not use 
    <b>LoadLibrary</b> to run an .exe file. Instead, use 
    the <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function.

If the specified module is a DLL that is not already loaded for the calling process, the system calls the 
    DLL's <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function with the 
    <b>DLL_PROCESS_ATTACH</b> value. If 
    <b>DllMain</b> returns <b>TRUE</b>, 
    <b>LoadLibrary</b> returns a handle to the module. If 
    <b>DllMain</b> returns <b>FALSE</b>, 
    the system unloads the DLL from the process address space and 
    <b>LoadLibrary</b> returns <b>NULL</b>. It is 
    not safe to call <b>LoadLibrary</b> from 
    <b>DllMain</b>. For more information, see the Remarks section in 
    <b>DllMain</b>.

Module handles are not global or inheritable. A call to 
    <b>LoadLibrary</b> by one process does not produce a handle that 
    another process can use — for example, in calling 
    <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>. The other process must make its own 
    call to <b>LoadLibrary</b> for the module before calling 
    <b>GetProcAddress</b>.

If <i>lpFileName</i> does not include a path and there is more than one loaded module with 
    the same base name and extension, the function returns a handle to the module that was loaded first.

If no file name extension is specified in the <i>lpFileName</i> parameter, the default 
    library extension .dll is appended. However, the file name string can include a trailing point character (.) to 
    indicate that the module name has no extension. When no path is specified, the function searches for loaded 
    modules whose base name matches the base name of the module to be loaded. If the name matches, the load succeeds. 
    Otherwise, the function searches for the file.

The first directory searched is the directory containing the image file used to create the calling process 
    (for more information, see the 
    <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function). Doing this allows 
    private dynamic-link library (DLL) files associated with a process to be found without adding the process's 
    installed directory to the PATH environment variable. If a relative path is 
    specified, the entire relative path is appended to every token in the DLL search path list. To load a module from 
    a relative path without searching any other path, use 
    <a href="https://msdn.microsoft.com/4cf59ee3-4065-4096-a2b5-fbed20aa5caa">GetFullPathName</a> to get a nonrelative path and call 
    <b>LoadLibrary</b> with the nonrelative path. For more 
    information on the DLL search order, see 
    <a href="https://msdn.microsoft.com/44228cf2-6306-466c-8f16-f513cd3ba8b5">Dynamic-Link Library Search Order</a>.

The search path can be altered using the 
    <a href="https://msdn.microsoft.com/c0c57554-3d98-487c-8bae-c594620d5a00">SetDllDirectory</a> function. This solution is recommended 
    instead of using <a href="https://msdn.microsoft.com/en-us/library/Aa365530(v=VS.85).aspx">SetCurrentDirectory</a> or 
    hard-coding the full path to the DLL.

If a path is specified and there is a redirection file for the application, the function searches for the 
    module in the application's directory. If the module exists in the application's directory, 
    <b>LoadLibrary</b> ignores the specified path and loads the 
    module from the application's directory. If the module does not exist in the application's directory, 
    <b>LoadLibrary</b> loads the module from the specified 
    directory. For more information, see 
    <a href="https://msdn.microsoft.com/3b426b6c-1ad5-43b9-81ea-5e6d3c6588c8">Dynamic Link Library Redirection</a>.

 If you call <b>LoadLibrary</b> with the name of an assembly 
    without a path specification and the assembly is listed in the system compatible manifest, the call is 
    automatically redirected to the side-by-side assembly.

The system maintains a per-process reference 
    count on all loaded modules. Calling <b>LoadLibrary</b> 
    increments the reference count. Calling the <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a> or 
    <a href="https://msdn.microsoft.com/be63fdbf-b3a4-44a8-99b4-b41e159952a7">FreeLibraryAndExitThread</a> function decrements 
    the reference count. The system unloads a module when its reference count reaches zero or when the process 
    terminates (regardless of the reference count).

<b>Windows Server 2003 and Windows XP:  </b>The Visual C++ compiler supports a syntax that enables you to declare thread-local variables: 
      <b>_declspec(thread)</b>. If you use this syntax in a DLL, you will not be able to load the 
      DLL explicitly using <b>LoadLibrary</b> on versions of Windows 
      prior to Windows Vista. If your DLL will be loaded explicitly, you must use the thread local 
      storage functions instead of <b>_declspec(thread)</b>. For an example, see 
      <a href="https://msdn.microsoft.com/a300f223-b513-4a22-a7a4-5d98cf74d77d">Using Thread Local Storage 
      in a Dynamic Link Library</a>.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
Do not use the <a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a> function to retrieve a path to 
      a DLL for a subsequent <b>LoadLibrary</b> call. The 
      <b>SearchPath</b> function uses a different search order than 
      <b>LoadLibrary</b> and it does not use safe process search mode 
      unless this is explicitly enabled by calling 
      <a href="https://msdn.microsoft.com/1874933d-92c3-4945-a3e4-e6dede232d5e">SetSearchPathMode</a> with 
      <b>BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE</b>. Therefore, 
      <b>SearchPath</b> is likely to first search the user’s current 
      working directory for the specified DLL. If an attacker has copied a malicious version of a DLL into the current 
      working directory, the path retrieved by <b>SearchPath</b> will 
      point to the malicious DLL, which <b>LoadLibrary</b> will then 
      load.

Do not make assumptions about the operating system version based on a 
      <b>LoadLibrary</b> call that searches for a DLL. If the 
      application is running in an environment where the DLL is legitimately not present but a malicious version of 
      the DLL is in the search path, the malicious version of the DLL may be loaded. Instead, use the recommended 
      techniques described in 
      <a href="https://msdn.microsoft.com/ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a">Getting the System Version</a>.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/0ffce2b1-ce50-4550-aa68-6628fdcac01a">Using Run-Time Dynamic Linking</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>



<a href="https://msdn.microsoft.com/29e50bd5-1712-407f-bcb3-50a0a22ab8b5">Dynamic-Link Library Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648042(v=VS.85).aspx">FindResource</a>



<a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a>



<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a>



<a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648046(v=VS.85).aspx">LoadResource</a>



<a href="https://msdn.microsoft.com/81e237a9-3c32-46a5-88d3-c978f43dad54">Run-Time Dynamic Linking</a>



<a href="https://msdn.microsoft.com/c0c57554-3d98-487c-8bae-c594620d5a00">SetDllDirectory</a>



<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>
 

 

