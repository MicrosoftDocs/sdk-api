---
UID: NF:dbghelp.SymEnumerateModulesW64
title: SymEnumerateModulesW64 function
author: windows-sdk-content
description: Enumerates all modules that have been loaded for the process by the SymLoadModule64 or SymLoadModuleEx function.
old-location: base\symenumeratemodules64.htm
tech.root: Debug
ms.assetid: d2372521-eff7-4ac4-a0f3-1267ef50db6e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymEnumerateModules, SymEnumerateModules function, SymEnumerateModules64, SymEnumerateModules64 function, SymEnumerateModulesW64, _win32_symenumeratemodules64, base.symenumeratemodules64, dbghelp/SymEnumerateModules, dbghelp/SymEnumerateModules64, dbghelp/SymEnumerateModulesW64
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
req.unicode-ansi: SymEnumerateModulesW64 (Unicode) and SymEnumerateModules64 (ANSI)
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
 - SymEnumerateModules64
 - SymEnumerateModules64
 - SymEnumerateModulesW64
 - SymEnumerateModules
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymEnumerateModulesW64 function


## -description


Enumerates all modules that have been loaded for the process by the 
<a href="https://msdn.microsoft.com/be50588b-066b-42ab-ba81-7537c811676f">SymLoadModule64</a> or <a href="https://msdn.microsoft.com/4a880090-f063-4d03-8fd5-a57ccba262c8">SymLoadModuleEx</a> function.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param EnumModulesCallback [in]

The enumeration callback function. This function is called once per module. For more information, see 
<a href="https://msdn.microsoft.com/97a82134-7e1b-4c7e-aa55-8347fea4e739">SymEnumerateModulesProc64</a>.


### -param UserContext [in, optional]

A user-defined value or <b>NULL</b>. This value is simply passed to the callback function. Normally, this parameter is used by an application to pass a pointer to a data structure that lets the callback function establish some type of context.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SymEnumerateModules64</b> function enumerates all modules that have been loaded for the process by 
<a href="https://msdn.microsoft.com/be50588b-066b-42ab-ba81-7537c811676f">SymLoadModule64</a>, even if the symbol loading is deferred. The enumeration callback function is called once for each module and is passed the module information.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR. <b>SymEnumerateModulesW64</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BOOL
IMAGEAPI
SymEnumerateModulesW64(
    __in HANDLE hProcess,
    __in PSYM_ENUMMODULES_CALLBACKW64 EnumModulesCallback,
    __in_opt PVOID UserContext
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
#define SymEnumerateModules64  SymEnumerateModulesW64
#endif</pre>
</td>
</tr>
</table></span></div>
This function supersedes the <b>SymEnumerateModules</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymEnumerateModules</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define SymEnumerateModules SymEnumerateModules64
#else
BOOL
IMAGEAPI
SymEnumerateModules(
    __in HANDLE hProcess,
    __in PSYM_ENUMMODULES_CALLBACK EnumModulesCallback,
    __in_opt PVOID UserContext
    );
#endif</pre>
</td>
</tr>
</table></span></div>

#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/8c7fdfaa-d4d3-42d6-ad19-23e8ffda7bf4">Enumerating Symbol Modules</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/97a82134-7e1b-4c7e-aa55-8347fea4e739">SymEnumerateModulesProc64</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>



<a href="https://msdn.microsoft.com/be50588b-066b-42ab-ba81-7537c811676f">SymLoadModule64</a>
 

 

