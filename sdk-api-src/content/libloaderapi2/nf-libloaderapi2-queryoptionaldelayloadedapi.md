---
UID: NF:libloaderapi2.QueryOptionalDelayLoadedAPI
title: QueryOptionalDelayLoadedAPI function
author: windows-sdk-content
description: Determines whether the specified function in a delay-loaded DLL is available on the system.
old-location: base\queryoptionaldelayloadedapi.htm
old-project: Dlls
ms.assetid: 43690689-4372-48ae-ac6d-230250f05f7c
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: QueryOptionalDelayLoadedAPI, QueryOptionalDelayLoadedAPI function, base.queryoptionaldelayloadedapi, libloaderapi2/QueryOptionalDelayLoadedAPI
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: libloaderapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: L2_NOTIFICATION_DATA, *PL2_NOTIFICATION_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	api-ms-win-core-libraryloader-l1-1-1.dll
-	kernelbase.dll
-	api-ms-win-core-libraryloader-l2-1-0.dll
-	API-MS-Win-Core-LibraryLoader-Private-L1-1-0.dll
api_name:
-	QueryOptionalDelayLoadedAPI
product: Windows
targetos: Windows
req.lib: WindowsApp.lib
req.dll: Api-ms-win-core-libraryloader-l1-1-1.dll
req.irql: 
req.product: GDI+ 1.1
---

# QueryOptionalDelayLoadedAPI function


## -description


Determines whether the specified function in a delay-loaded DLL is available on the system. 


## -parameters




### -param hParentModule [in]

A handle to the calling module. Desktop applications can use the <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> or <a href="https://msdn.microsoft.com/951c7e6e-1d6d-4393-a675-d2b353c53b87">GetModuleHandleEx</a> function to get this handle. Windows Store apps should set this parameter to <code>static_cast&lt;HMODULE&gt;(&amp;__ImageBase)</code>.


### -param lpDllName [in]

The file name of the delay-loaded DLL that exports the specified function. This parameter is case-insensitive.

Windows Store apps should specify API sets, rather than monolithic DLLs. For example,   api-ms-win-core-memory-l1-1-1.dll, rather than kernel32.dll.


### -param lpProcName [in]

The name of the function to query. This parameter is case-sensitive.


### -param Reserved

This parameter is reserved and must be zero (0).


## -returns



TRUE if the specified function is available on the system. If the specified function is not available on the system, this function returns FALSE. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A delay-loaded DLL is statically linked but not actually loaded into memory until the running application references a symbol exported by that DLL. Applications often delay load DLLs that contain functions the application might call only rarely or not at all, because the DLL is only loaded when it is needed instead of being loaded at application startup like other statically linked DLLs. This helps improve application performance, especially during initialization. A delay-load DLL is specified at link time with the <a href="https://go.microsoft.com/fwlink/p/?linkid=231328">/DELAYLOAD (Delay Load Import)</a> linker option. 

Applications that target multiple versions of Windows or multiple Windows device families also rely on delay-loaded DLLs to make visible extra features when they are available.

A desktop application can use delayed loading as an alternative to runtime dynamic linking that uses  <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> or <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a> to load a DLL and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to get a pointer to a function. A Windows Store app cannot use <b>LoadLibrary</b> or <b>LoadLibraryEx</b>, so to get the benefits to runtime dynamic linking, a Windows Store app must use the delayed loading mechanism.

To check whether a function in a delay-loaded DLL is available on the system, the application calls <b>QueryOptionalDelayLoadedAPI</b> with the specified function. If <b>QueryOptionalDelayLoadedAPI</b> succeeds, the application can safely call the specified function. 


#### Examples

The following example shows how to use <b>QueryOptionalDelayLoadedAPI</b> to determine whether the <a href="https://msdn.microsoft.com/ff0b6b79-40f5-499c-b797-b66797654164">VirtualAllocEx</a> function is available on the system.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;libloaderapi2.h&gt;

// For this example, you need to pass
// /delayload: ext-ms-win-com-ole32-l1-1-1.dll to link.exe.

EXTERN_C IMAGE_DOS_HEADER __ImageBase;

BOOL
AreMonikersSupported ()
{

    BOOL isApiAvailable;

    // Check if MkParseDisplayName is available on the system. It is only
    // available on desktop computers, and not on mobile devices or Xbox.

    isApiAvailable = 
        QueryOptionalDelayLoadedAPI(static_cast&lt;HMODULE&gt;(&amp;__ImageBase),
                                    "ext-ms-win-com-ole32-l1-1-1.dll",
                                    "MkParseDisplayName",
                                    0);

    return isApiAvailable;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4a103753-a2c9-487f-b797-01d5f5d489f3">LoadPackagedLibrary</a>



<a href="https://msdn.microsoft.com/81e237a9-3c32-46a5-88d3-c978f43dad54">Run-Time Dynamic Linking</a>
 

 

