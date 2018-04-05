---
UID: NC:dbghelp.PFUNCTION_TABLE_ACCESS_ROUTINE64
title: PFUNCTION_TABLE_ACCESS_ROUTINE64
author: windows-driver-content
description: An application-defined callback function used with the StackWalk64 function. It provides access to the run-time function table for the process.
old-location: base\functiontableaccessproc64.htm
old-project: Debug
ms.assetid: 387c20b0-ed16-463c-8b11-3ac9a43548a1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FunctionTableAccessProc64, FunctionTableAccessProc64 callback function, PFUNCTION_TABLE_ACCESS_ROUTINE, PFUNCTION_TABLE_ACCESS_ROUTINE64, _win32_functiontableaccessproc64, base.functiontableaccessproc64, dbghelp/FunctionTableAccessProc64
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DAV_CALLBACK_CRED, *PDAV_CALLBACK_CRED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	DbgHelp.h
api_name:
-	FunctionTableAccessProc64
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PFUNCTION_TABLE_ACCESS_ROUTINE64 callback


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a> function. It provides access to the run-time function table for the process.

The <b>PFUNCTION_TABLE_ACCESS_ROUTINE64</b> type defines a pointer to this callback function. 
<b>FunctionTableAccessProc64</b> is a placeholder for the application-defined function name.


## -parameters




### -param ahProcess


### -param AddrBase [in]

The address of the instruction to be located.


#### - hProcess [in]

A handle to the process for which the stack trace is generated.


## -returns



The function returns a pointer to the run-time function table. On an x86 computer, this is a pointer to an 
<a href="https://msdn.microsoft.com/916dc7d5-ed88-4573-b696-fd00bbf4e086">FPO_DATA</a> structure. On an Alpha computer, this is a pointer to an 
<a href="https://msdn.microsoft.com/ced956ec-7a12-4548-8e38-a1c1057c05e8">IMAGE_FUNCTION_ENTRY</a> structure.




## -remarks



This callback function supersedes the <i>PFUNCTION_TABLE_ACCESS_ROUTINE</i> callback function.  <i>PFUNCTION_TABLE_ACCESS_ROUTINE</i> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define PFUNCTION_TABLE_ACCESS_ROUTINE PFUNCTION_TABLE_ACCESS_ROUTINE64
#else
typedef
PVOID
(__stdcall *PFUNCTION_TABLE_ACCESS_ROUTINE)(
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



<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a>
 

 

