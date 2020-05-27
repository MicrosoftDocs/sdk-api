---
UID: NF:libloaderapi.GetModuleHandleExW
title: GetModuleHandleExW function (libloaderapi.h)
description: Retrieves a module handle for the specified module and increments the module's reference count unless GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT is specified. The module must have been loaded by the calling process.
helpviewer_keywords: ["GET_MODULE_HANDLE_EX_FLAG_FROM_ADDRESS","GET_MODULE_HANDLE_EX_FLAG_PIN","GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT","GetModuleHandleEx","GetModuleHandleEx function","GetModuleHandleExA","GetModuleHandleExW","_win32_getmodulehandleex","base.getmodulehandleex","libloaderapi/GetModuleHandleEx","libloaderapi/GetModuleHandleExA","libloaderapi/GetModuleHandleExW","winbase/GetModuleHandleEx","winbase/GetModuleHandleExA","winbase/GetModuleHandleExW"]
old-location: base\getmodulehandleex.htm
tech.root: Dlls
ms.assetid: 951c7e6e-1d6d-4393-a675-d2b353c53b87
ms.date: 12/05/2018
ms.keywords: GET_MODULE_HANDLE_EX_FLAG_FROM_ADDRESS, GET_MODULE_HANDLE_EX_FLAG_PIN, GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT, GetModuleHandleEx, GetModuleHandleEx function, GetModuleHandleExA, GetModuleHandleExW, _win32_getmodulehandleex, base.getmodulehandleex, libloaderapi/GetModuleHandleEx, libloaderapi/GetModuleHandleExA, libloaderapi/GetModuleHandleExW, winbase/GetModuleHandleEx, winbase/GetModuleHandleExA, winbase/GetModuleHandleExW
f1_keywords:
- libloaderapi/GetModuleHandleEx
dev_langs:
- c++
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetModuleHandleExW (Unicode) and GetModuleHandleExA (ANSI)
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
- API-MS-Win-Core-LibraryLoader-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-LibraryLoader-l1-1-1.dll
- API-MS-Win-Core-LibraryLoader-l1-2-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
- API-MS-Win-Core-Libraryloader-l1-2-1.dll
- API-MS-Win-Core-LibraryLoader-L1-2-2.dll
- vertdll.dll
api_name:
- GetModuleHandleEx
- GetModuleHandleExA
- GetModuleHandleExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetModuleHandleExW function


## -description


Retrieves a module handle for the specified module and increments the module's reference count unless GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT is specified. The module must have been loaded by the calling process.


## -parameters




### -param dwFlags [in]

This parameter can be zero or one or more of the following values. If the module's reference count is incremented, the caller must use the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> function to decrement the reference count when the module handle is no longer needed.



#### GET_MODULE_HANDLE_EX_FLAG_FROM_ADDRESS (0x00000004)

The <i>lpModuleName</i> parameter is an address in the module.



#### GET_MODULE_HANDLE_EX_FLAG_PIN (0x00000001)

The module stays loaded until the process is terminated, no matter how many times 
<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> is called. 




This option cannot be used with GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT.



#### GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT (0x00000002)

The reference count for the module is not incremented. This option is equivalent to the behavior of 
<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>. Do not pass the retrieved module handle to the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> function; doing so can cause the DLL to be unmapped prematurely. For more information, see Remarks. 




This option cannot be used with GET_MODULE_HANDLE_EX_FLAG_PIN.


### -param lpModuleName [in, optional]

The name of the loaded module (either a .dll or .exe file), or an address in the module (if <i>dwFlags</i> is GET_MODULE_HANDLE_EX_FLAG_FROM_ADDRESS). 




For a module name, if the file name extension is omitted, the default library extension .dll is appended. The file name string can include a trailing point character (.) to indicate that the module name has no extension. The string does not have to specify a path. When specifying a path, be sure to use backslashes (\), not forward slashes (/). The name is compared (case independently) to the names of modules currently mapped into the address space of the calling process.

If this parameter is NULL, the function returns a handle to the file used to create the calling process (.exe file).


### -param phModule [out]

A handle to the specified module. If the function fails, this parameter is NULL.

The <b>GetModuleHandleEx</b> function does not retrieve handles for modules that were loaded using the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>.


##### - dwFlags.GET_MODULE_HANDLE_EX_FLAG_FROM_ADDRESS (0x00000004)

The <i>lpModuleName</i> parameter is an address in the module.


##### - dwFlags.GET_MODULE_HANDLE_EX_FLAG_PIN (0x00000001)

The module stays loaded until the process is terminated, no matter how many times 
<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> is called. 




This option cannot be used with GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT.


##### - dwFlags.GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT (0x00000002)

The reference count for the module is not incremented. This option is equivalent to the behavior of 
<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>. Do not pass the retrieved module handle to the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> function; doing so can cause the DLL to be unmapped prematurely. For more information, see Remarks. 




This option cannot be used with GET_MODULE_HANDLE_EX_FLAG_PIN.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, see 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The handle returned is not global or inheritable. It cannot be duplicated or used by another process.

If <i>lpModuleName</i> does not include a path and there is more than one loaded module with the same base name and extension, you cannot predict which module handle will be returned. To work around this problem, you could specify a path, use <a href="https://docs.microsoft.com/windows/desktop/Msi/side-by-side-assemblies">side-by-side assemblies</a>, or specify a memory location rather than a DLL name in the <i>lpModuleName</i> parameter. 

If <i>dwFlags</i> contains GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT, the <b>GetModuleHandleEx</b> function returns a handle to a mapped module without incrementing its reference count. However, if this handle is passed to the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> function, the reference count of the mapped module will be decremented. Therefore, do not pass a handle returned by <b>GetModuleHandleEx</b> with GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT to the 
<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> function. Doing so can cause a DLL module to be unmapped prematurely.

If <i>dwFlags</i> contains GET_MODULE_HANDLE_EX_UNCHANGED_REFCOUNT, this function must be used carefully in a multithreaded application. There is no guarantee that the module handle remains valid between the time this function returns the handle and the time it is used. For example, a thread retrieves a module handle, but before it uses the handle, a second thread frees the module. If the system loads another module, it could reuse the module handle that was recently freed. Therefore, first thread would have a handle to a module different than the one intended.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Dlls/dynamic-link-library-functions">Dynamic-Link Library Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea">GetModuleFileName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>
 

 

