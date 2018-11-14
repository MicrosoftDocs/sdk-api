---
UID: NF:dbghelp.SymGetModuleBase
title: SymGetModuleBase function
author: windows-sdk-content
description: Retrieves the base address of the module that contains the specified address.
old-location: base\symgetmodulebase64.htm
tech.root: debug
ms.assetid: 964d0fdb-d982-4509-8c49-0ad0a3491226
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: SymGetModuleBase, SymGetModuleBase function, SymGetModuleBase64, SymGetModuleBase64 function, _win32_symgetmodulebase64, base.symgetmodulebase64, dbghelp/SymGetModuleBase, dbghelp/SymGetModuleBase64
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
req.unicode-ansi: 
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
 - SymGetModuleBase64
 - SymGetModuleBase
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
- apiref
: 
- 
: 
- SymGetModuleBase
: 
---

# SymGetModuleBase function


## -description


Retrieves the base address of the module that contains the specified address.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param dwAddr

TBD




#### - qwAddr [in]

The virtual address that is contained in one of the modules loaded by the 
<a href="https://msdn.microsoft.com/be50588b-066b-42ab-ba81-7537c811676f">SymLoadModule64</a> function.


## -returns



If the function succeeds, the return value is a nonzero virtual address. The value is the base address of the module containing the address specified by the <i>dwAddr</i> parameter.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The module table is searched for a module that contains <i>dwAddr</i>. The module is located based on the load address and size of each module.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymGetModuleBase</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymGetModuleBase</b> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define SymGetModuleBase SymGetModuleBase64
#else
DWORD
IMAGEAPI
SymGetModuleBase(
    __in HANDLE hProcess,
    __in DWORD dwAddr
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>



<a href="https://msdn.microsoft.com/be50588b-066b-42ab-ba81-7537c811676f">SymLoadModule64</a>
 

 

