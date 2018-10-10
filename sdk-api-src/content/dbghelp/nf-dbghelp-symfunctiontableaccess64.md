---
UID: NF:dbghelp.SymFunctionTableAccess64
title: SymFunctionTableAccess64 function
author: windows-sdk-content
description: Retrieves the function table entry for the specified address.
old-location: base\symfunctiontableaccess64.htm
tech.root: debug
ms.assetid: f79e6af9-9931-4bd7-ae12-29d890267a89
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: SymFunctionTableAccess, SymFunctionTableAccess function, SymFunctionTableAccess64, SymFunctionTableAccess64 function, _win32_symfunctiontableaccess64, base.symfunctiontableaccess64, dbghelp/SymFunctionTableAccess, dbghelp/SymFunctionTableAccess64
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
 - SymFunctionTableAccess64
 - SymFunctionTableAccess
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymFunctionTableAccess64 function


## -description


Retrieves the function table entry for the specified address.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param AddrBase [in]

The base address for which function table information is required.


## -returns



If the function succeeds, the return value is a pointer to the function table entry.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The type of pointer returned is specific to the image from which symbols are loaded. 

<b>x86:  </b>If the image is for an x86 system, this is a pointer to an 
<a href="https://msdn.microsoft.com/916dc7d5-ed88-4573-b696-fd00bbf4e086">FPO_DATA</a> structure.

<b>x64:  </b>If the image is for an x64 system, this is a pointer to an <a href="https://msdn.microsoft.com/9ed16f9a-3403-4ba9-9968-f51f6788a1f8">_IMAGE_RUNTIME_FUNCTION_ENTRY</a> structure.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymFunctionTableAccess</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymFunctionTableAccess</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define SymFunctionTableAccess SymFunctionTableAccess64
#else
PVOID
IMAGEAPI
SymFunctionTableAccess(
    __in HANDLE hProcess,
    __in DWORD AddrBase
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/916dc7d5-ed88-4573-b696-fd00bbf4e086">FPO_DATA</a>



<a href="https://msdn.microsoft.com/ced956ec-7a12-4548-8e38-a1c1057c05e8">IMAGE_FUNCTION_ENTRY</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>



<a href="https://msdn.microsoft.com/9ed16f9a-3403-4ba9-9968-f51f6788a1f8">_IMAGE_RUNTIME_FUNCTION_ENTRY</a>
 

 

