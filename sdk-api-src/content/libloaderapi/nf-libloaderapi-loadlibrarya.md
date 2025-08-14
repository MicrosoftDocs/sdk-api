---
UID: NF:libloaderapi.LoadLibraryA
title: LoadLibraryA function (libloaderapi.h)
description: Loads the specified module into the address space of the calling process. (LoadLibraryA)
helpviewer_keywords: ["LoadLibraryA", "libloaderapi/LoadLibraryA"]
old-location: base\loadlibrary.htm
tech.root: base
ms.assetid: d936b4dd-058c-48e1-834b-b47ef6d8ef65
ms.date: 12/05/2018
ms.keywords: LoadLibrary, LoadLibrary function, LoadLibraryA, LoadLibraryW, _win32_loadlibrary, base.loadlibrary, libloaderapi/LoadLibrary, libloaderapi/LoadLibraryA, libloaderapi/LoadLibraryW, winbase/LoadLibrary, winbase/LoadLibraryA, winbase/LoadLibraryW
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
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
 - LoadLibraryA
 - libloaderapi/LoadLibraryA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-libraryloader-l1-2-3.dll
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
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
---

# LoadLibraryA function


## -description

Loads the specified  module into the address space of the calling process. The specified
    module may cause other modules to be loaded.

For additional load options, use the
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> function.

## -parameters

### -param lpLibFileName [in]

The name of the module. This can be either a library module (a .dll file) or an executable
module (an .exe file).
If the specified module is an executable module, static imports are not loaded;
instead, the module is loaded as if by
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>
with the `DONT_RESOLVE_DLL_REFERENCES` flag.

The name specified is the file name of the module and is not related to the
       name stored in the library module itself, as specified by the <b>LIBRARY</b> keyword in
       the module-definition (.def) file.

If the string specifies a full path, the function searches only that path for the module.

If the string specifies a relative path or a module name without a path, the function uses a standard search
       strategy to find the module; for more information, see the Remarks.

If the function cannot find the  module, the function fails. When specifying a path, be sure to use
       backslashes (\\), not forward slashes (/). For more information about paths, see
       <a href="/windows/desktop/FileIO/naming-a-file">Naming a File or Directory</a>.

If the string specifies a module name without a path and the file name extension is omitted, the function
       appends the default library extension ".DLL" to the module name. To prevent the function from appending
       ".DLL" to the module name, include a trailing point character (.) in the module name string.

## -returns

If the function succeeds, the return value is a handle to the module.

If the function fails, the return value is NULL. To get extended error information, call
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To enable or disable error messages displayed by the loader during DLL loads, use the
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a> function.

<b>LoadLibrary</b> can be used to load a library module into
    the address space of the process and return a handle that can be used in
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to get the address of a DLL function.
    <b>LoadLibrary</b> can also be used to load other executable
    modules. For example, the function can specify an .exe file to get a handle that can be used in
    <a href="/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a> or
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>. However, do not use
    <b>LoadLibrary</b> to run an .exe file. Instead, use
    the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function.

If the specified module is a DLL that is not already loaded for the calling process, the system calls the
    DLL's <a href="/windows/desktop/Dlls/dllmain">DllMain</a> function with the
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
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>. The other process must make its own
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
    <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function). Doing this allows
    private dynamic-link library (DLL) files associated with a process to be found without adding the process's
    installed directory to the PATH environment variable. If a relative path is
    specified, the entire relative path is appended to every token in the DLL search path list. To load a module from
    a relative path without searching any other path, use
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a> to get a nonrelative path and call
    <b>LoadLibrary</b> with the nonrelative path. For more
    information on the DLL search order, see
    <a href="/windows/desktop/Dlls/dynamic-link-library-search-order">Dynamic-Link Library Search Order</a>.

The search path can be altered using the
    <a href="/windows/desktop/api/winbase/nf-winbase-setdlldirectorya">SetDllDirectory</a> function. This solution is recommended
    instead of using <a href="/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory">SetCurrentDirectory</a> or
    hard-coding the full path to the DLL.

If a path is specified and there is a redirection file for the application, the function searches for the
    module in the application's directory. If the module exists in the application's directory,
    <b>LoadLibrary</b> ignores the specified path and loads the
    module from the application's directory. If the module does not exist in the application's directory,
    <b>LoadLibrary</b> loads the module from the specified
    directory. For more information, see
    <a href="/windows/desktop/Dlls/dynamic-link-library-redirection">Dynamic Link Library Redirection</a>.

 If you call <b>LoadLibrary</b> with the name of an assembly
    without a path specification and the assembly is listed in the system compatible manifest, the call is
    automatically redirected to the side-by-side assembly.

The system maintains a per-process reference
    count on all loaded modules. Calling <b>LoadLibrary</b>
    increments the reference count. Calling the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> or
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread">FreeLibraryAndExitThread</a> function decrements
    the reference count. The system unloads a module when its reference count reaches zero or when the process
    terminates (regardless of the reference count).

<b>Windows Server 2003 and Windows XP:  </b>The Visual C++ compiler supports a syntax that enables you to declare thread-local variables:
      <b>_declspec(thread)</b>. If you use this syntax in a DLL, you will not be able to load the
      DLL explicitly using <b>LoadLibrary</b> on versions of Windows
      prior to Windows Vista. If your DLL will be loaded explicitly, you must use the thread local
      storage functions instead of <b>_declspec(thread)</b>. For an example, see
      <a href="/windows/desktop/Dlls/using-thread-local-storage-in-a-dynamic-link-library">Using Thread Local Storage
      in a Dynamic Link Library</a>.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
Do not use the <a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a> function to retrieve a path to
      a DLL for a subsequent <b>LoadLibrary</b> call. The
      <b>SearchPath</b> function uses a different search order than
      <b>LoadLibrary</b> and it does not use safe process search mode
      unless this is explicitly enabled by calling
      <a href="/windows/desktop/api/winbase/nf-winbase-setsearchpathmode">SetSearchPathMode</a> with
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
      <a href="/windows/desktop/SysInfo/getting-the-system-version">Getting the System Version</a>.


#### Examples

For an example, see
     <a href="/windows/desktop/Dlls/using-run-time-dynamic-linking">Using Run-Time Dynamic Linking</a>.

<div class="code"></div>




> [!NOTE]
> The libloaderapi.h header defines LoadLibrary as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Dlls/dllmain">DllMain</a>



<a href="/windows/desktop/Dlls/dynamic-link-library-functions">Dynamic-Link Library Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya">GetSystemDirectory</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>



<a href="/windows/desktop/Dlls/run-time-dynamic-linking">Run-Time Dynamic Linking</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setdlldirectorya">SetDllDirectory</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a>
