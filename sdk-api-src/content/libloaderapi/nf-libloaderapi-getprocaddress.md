---
UID: NF:libloaderapi.GetProcAddress
title: GetProcAddress function (libloaderapi.h)
author: windows-sdk-content
description: Retrieves the address of an exported function or variable from the specified dynamic-link library (DLL).
old-location: base\getprocaddress.htm
tech.root: Dlls
ms.assetid: a0d7fc09-f888-4f46-a571-d3719a627597
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetProcAddress, GetProcAddress function, _win32_getprocaddress, base.getprocaddress, libloaderapi/GetProcAddress, winbase/GetProcAddress
ms.topic: function
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
api_name:
 - GetProcAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetProcAddress function


## -description


Retrieves the address of an exported function or variable from the specified dynamic-link library (DLL).


## -parameters




### -param hModule [in]

A handle to the DLL module that contains the function or variable. The 
<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>, <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>, <a href="https://msdn.microsoft.com/4a103753-a2c9-487f-b797-01d5f5d489f3">LoadPackagedLibrary</a>, or 
<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> function returns this handle. 

The <b>GetProcAddress</b> function does not retrieve addresses from modules that were loaded using the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>.


### -param lpProcName [in]

The function or variable name, or the function's ordinal value. If this parameter is an ordinal value, it must be in the low-order word; the high-order word must be zero.


## -returns



If the function succeeds, the return value is the address of the exported function or variable.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The spelling and case of a function name pointed to by <i>lpProcName</i> must be identical to that in the <b>EXPORTS</b> statement of the source DLL's module-definition (.def) file. The exported names of functions may differ from the names you use when calling these functions in your code. This difference is hidden by macros used in the SDK header files. For more information, see 
<a href="https://msdn.microsoft.com/601d24b0-11bb-48fa-a257-207c3acee226">Conventions for Function Prototypes</a>.

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


For the complete example that contains this code fragment, see <a href="https://msdn.microsoft.com/ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a">Getting the System Version</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/0ffce2b1-ce50-4550-aa68-6628fdcac01a">Using Run-Time Dynamic Linking</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/29e50bd5-1712-407f-bcb3-50a0a22ab8b5">Dynamic-Link Library Functions</a>



<a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>



<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>



<a href="https://msdn.microsoft.com/4a103753-a2c9-487f-b797-01d5f5d489f3">LoadPackagedLibrary</a>



<a href="https://msdn.microsoft.com/81e237a9-3c32-46a5-88d3-c978f43dad54">Run-Time Dynamic Linking</a>
 

 

