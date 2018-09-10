---
UID: NC:dbghelp.PSYM_ENUMMODULES_CALLBACKW64
title: PSYM_ENUMMODULES_CALLBACKW64
author: windows-sdk-content
description: An application-defined callback function used with the SymEnumerateModules64 function. It is called once for each enumerated module, and receives the module information.
old-location: base\symenumeratemodulesproc64.htm
tech.root: debug
ms.assetid: 97a82134-7e1b-4c7e-aa55-8347fea4e739
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: PSYM_ENUMMODULES_CALLBACK, PSYM_ENUMMODULES_CALLBACK64, PSYM_ENUMMODULES_CALLBACKW64, SymEnumerateModulesProc64, SymEnumerateModulesProc64 callback, SymEnumerateModulesProc64 callback function, _win32_symenumeratemodulesproc64, base.symenumeratemodulesproc64, dbghelp/SymEnumerateModulesProc64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - SymEnumerateModulesProc64
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# PSYM_ENUMMODULES_CALLBACKW64 callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/d2372521-eff7-4ac4-a0f3-1267ef50db6e">SymEnumerateModules64</a> function. It is called once for each enumerated module, and receives the module information.

The <b>PSYM_ENUMMODULES_CALLBACK64</b> and <b>PSYM_ENUMMODULES_CALLBACKW64</b> types define a pointer to this callback function. 
<b>SymEnumerateModulesProc64</b> is a placeholder for the application-defined function name.


## -parameters




### -param ModuleName [in]

The name of the module.


### -param BaseOfDll [in]

The base address where the module is loaded into memory.


### -param UserContext [in, optional]

The user-defined value specified in 
<a href="https://msdn.microsoft.com/d2372521-eff7-4ac4-a0f3-1267ef50db6e">SymEnumerateModules64</a>, or <b>NULL</b>. Typically, this parameter is used by an application to pass a pointer to a data structure that lets the callback function establish some type of context.


## -returns



If the return value is <b>TRUE</b>, the enumeration will continue.

If the return value is <b>FALSE</b>, the enumeration will stop.




## -remarks



The calling application is called once per module until all modules are enumerated, or until the enumeration callback function returns <b>FALSE</b>.

This callback function supersedes the <i>PSYM_ENUMMODULES_CALLBACK</i> callback function.  <i>PSYM_ENUMMODULES_CALLBACK</i> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define PSYM_ENUMMODULES_CALLBACK PSYM_ENUMMODULES_CALLBACK64
#else
typedef BOOL
(CALLBACK *PSYM_ENUMMODULES_CALLBACK)(
    __in PCSTR ModuleName,
    __in ULONG BaseOfDll,
    __in_opt PVOID UserContext
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/d2372521-eff7-4ac4-a0f3-1267ef50db6e">SymEnumerateModules64</a>
 

 

