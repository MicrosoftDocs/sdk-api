---
UID: NF:libloaderapi.GetProcAddress
title: GetProcAddress function (libloaderapi.h)
description: Retrieves the address of an exported function or variable from the specified dynamic-link library (DLL).
helpviewer_keywords: ["GetProcAddress","GetProcAddress function","_win32_getprocaddress","base.getprocaddress","libloaderapi/GetProcAddress","winbase/GetProcAddress"]
old-location: base\getprocaddress.htm
tech.root: base
ms.assetid: a0d7fc09-f888-4f46-a571-d3719a627597
ms.date: 12/05/2018
ms.keywords: GetProcAddress, GetProcAddress function, _win32_getprocaddress, base.getprocaddress, libloaderapi/GetProcAddress, winbase/GetProcAddress
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - GetProcAddress
 - libloaderapi/GetProcAddress
dev_langs:
 - c++
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
 - GetProcAddress
---

# GetProcAddress function


## -description

Retrieves the address of an exported function (also known as a procedure) or variable from the specified dynamic-link library (DLL).

## -parameters

### -param hModule [in]

A handle to the DLL module that contains the function or variable. The 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>, <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>, <a href="/windows/desktop/api/winbase/nf-winbase-loadpackagedlibrary">LoadPackagedLibrary</a>, or 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a> function returns this handle. 

The <b>GetProcAddress</b> function does not retrieve addresses from modules that were loaded using the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>.

### -param lpProcName [in]

The function or variable name, or the function's ordinal value. If this parameter is an ordinal value, it must be in the low-order word; the high-order word must be zero.

## -returns

If the function succeeds, the return value is the address of the exported function or variable.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The spelling and case of a function name pointed to by <i>lpProcName</i> must be identical to that in the <b>EXPORTS</b> statement of the source DLL's module-definition (.def) file. The exported names of functions may differ from the names you use when calling these functions in your code. This difference is hidden by macros used in the SDK header files. For more information, see 
<a href="/windows/desktop/Intl/conventions-for-function-prototypes">Conventions for Function Prototypes</a>.

The <i>lpProcName</i> parameter can identify the DLL function by specifying an ordinal value associated with the function in the <b>EXPORTS</b> statement. 
<b>GetProcAddress</b> verifies that the specified ordinal is in the range 1 through the highest ordinal value exported in the .def file. The function then uses the ordinal as an index to read the function's address from a function table. 

If the .def file does not number the functions consecutively from 1 to <i>N</i> (where <i>N</i> is the number of exported functions), an error can occur where 
<b>GetProcAddress</b> returns an invalid, non-NULL address, even though there is no function with the specified ordinal.

If the function might not exist in the DLL module—for example, if the function  is available only on Windows Vista but the application  might be running on Windows XP—specify the function by name rather than by ordinal value and design your application to handle the case when the function is not available, as shown in the following code fragment.


```cpp

typedef void (WINAPI *PGNSI)(LPSYSTEM_INFO);

// Call GetNativeSystemInfo if supported or GetSystemInfo otherwise.

   PGNSI pGNSI;
   SYSTEM_INFO si;

   ZeroMemory(&si, sizeof(SYSTEM_INFO));
   
   pGNSI = (PGNSI) GetProcAddress(
      GetModuleHandle(TEXT("kernel32.dll")), 
      "GetNativeSystemInfo");
   if(NULL != pGNSI)
   {
      pGNSI(&si);
   }
   else 
   {
       GetSystemInfo(&si);
   }


```


For the complete example that contains this code fragment, see <a href="/windows/desktop/SysInfo/getting-the-system-version">Getting the System Version</a>.


#### Examples

For an example, see 
<a href="/windows/desktop/Dlls/using-run-time-dynamic-linking">Using Run-Time Dynamic Linking</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Dlls/dynamic-link-library-functions">Dynamic-Link Library Functions</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-loadpackagedlibrary">LoadPackagedLibrary</a>



<a href="/windows/desktop/Dlls/run-time-dynamic-linking">Run-Time Dynamic Linking</a>
