---
UID: NF:dbghelp.EnumerateLoadedModules64
title: EnumerateLoadedModules64 function
author: windows-sdk-content
description: Enumerates the loaded modules for the specified process.
old-location: base\enumerateloadedmodules64.htm
tech.root: debug
ms.assetid: 9bfa683f-2a0f-418f-8ac4-5c4224265f2e
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: EnumerateLoadedModules, EnumerateLoadedModules function, EnumerateLoadedModules64, EnumerateLoadedModules64 function, EnumerateLoadedModulesW64, _win32_enumerateloadedmodules64, base.enumerateloadedmodules64, dbghelp/EnumerateLoadedModules, dbghelp/EnumerateLoadedModules64, dbghelp/EnumerateLoadedModulesW64
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumerateLoadedModulesW64 (Unicode) and EnumerateLoadedModules64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - EnumerateLoadedModules64
 - EnumerateLoadedModules64
 - EnumerateLoadedModulesW64
 - EnumerateLoadedModules
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# EnumerateLoadedModules64 function


## -description


Enumerates the loaded modules for the specified process.


## -parameters




### -param hProcess [in]

A handle to the process whose modules will be enumerated.


### -param EnumLoadedModulesCallback [in]

An application-defined callback function. For more information, see 
<a href="https://msdn.microsoft.com/f6acb9cf-81f7-4b05-95e2-9628855f6b51">EnumerateLoadedModulesProc64</a>.


### -param UserContext [in, optional]

Optional user-defined data. This value is passed to the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, <i>EnumerateLoadedModulesW64</i>, define <b>DBGHELP_TRANSLATE_TCHAR</b>. <i>EnumerateLoadedModulesW64</i> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL
IMAGEAPI
EnumerateLoadedModulesW64(
    __in HANDLE hProcess,
    __in PENUMLOADED_MODULES_CALLBACKW64 EnumLoadedModulesCallback,
    __in PVOID UserContext
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
    #define EnumerateLoadedModules64      EnumerateLoadedModulesW64
#endif</pre>
</td>
</tr>
</table></span></div>
This function supersedes the <i>EnumerateLoadedModules</i> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <i>EnumerateLoadedModules</i> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define EnumerateLoadedModules EnumerateLoadedModules64
#else
BOOL
IMAGEAPI
EnumerateLoadedModules(
    __in HANDLE hProcess,
    __in PENUMLOADED_MODULES_CALLBACK EnumLoadedModulesCallback,
    __in_opt PVOID UserContext
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/f6acb9cf-81f7-4b05-95e2-9628855f6b51">EnumerateLoadedModulesProc64</a>
 

 

