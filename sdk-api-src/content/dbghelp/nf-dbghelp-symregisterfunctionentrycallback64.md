---
UID: NF:dbghelp.SymRegisterFunctionEntryCallback64
title: SymRegisterFunctionEntryCallback64 function
author: windows-sdk-content
description: Registers a callback function for use by the stack walking procedure on Alpha computers.
old-location: base\symregisterfunctionentrycallback64.htm
tech.root: debug
ms.assetid: 5915055f-2c6c-4a0e-ad0f-c5bd74558802
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SymRegisterFunctionEntryCallback, SymRegisterFunctionEntryCallback function, SymRegisterFunctionEntryCallback64, SymRegisterFunctionEntryCallback64 function, _win32_symregisterfunctionentrycallback64, base.symregisterfunctionentrycallback64, dbghelp/SymRegisterFunctionEntryCallback, dbghelp/SymRegisterFunctionEntryCallback64
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
 - imagehlp.dll
api_name:
 - SymRegisterFunctionEntryCallback64
 - SymRegisterFunctionEntryCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymRegisterFunctionEntryCallback64 function


## -description


Registers a callback function for use by the stack walking procedure on Alpha computers.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a> function.


### -param CallbackFunction [in]

A <a href="https://msdn.microsoft.com/cd10dfeb-451f-4d6d-ae1c-ecca75f86f3d">SymRegisterFunctionEntryCallbackProc64</a> callback function.


### -param UserContext [in]

A user-defined value or <b>NULL</b>. This value is simply passed to the callback function. Normally, this parameter is used by an application to pass a pointer to a data structure that lets the callback function establish some context.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SymRegisterFunctionEntryCallback64</b> function lets an application register a callback function for use by the stack walking procedure. The stack walking procedure calls the registered callback function when it is unable to locate a function table entry for an address. In most cases, the stack walking procedure locates the function table entries in the function table of the image containing the address. However, in situations where the function table entries are not in the image, this callback allows the debugger to provide the function table entry from another source. For example, run-time generated code on Alpha computers can define dynamic function tables to support exception handling and stack tracing.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymRegisterFunctionEntryCallback</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymRegisterFunctionEntryCallback</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define SymRegisterFunctionEntryCallback SymRegisterFunctionEntryCallback64
#else
BOOL
IMAGEAPI
SymRegisterFunctionEntryCallback(
    __in HANDLE hProcess,
    __in PSYMBOL_FUNCENTRY_CALLBACK CallbackFunction,
    __in_opt PVOID UserContext
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a>



<a href="https://msdn.microsoft.com/cd10dfeb-451f-4d6d-ae1c-ecca75f86f3d">SymRegisterFunctionEntryCallbackProc64</a>
 

 

