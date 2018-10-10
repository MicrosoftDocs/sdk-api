---
UID: NC:dbghelp.PTRANSLATE_ADDRESS_ROUTINE64
title: PTRANSLATE_ADDRESS_ROUTINE64
author: windows-sdk-content
description: An application-defined callback function used with the StackWalk64 function. It provides address translation for 16-bit addresses.
old-location: base\translateaddressproc64.htm
tech.root: debug
ms.assetid: 56c374df-6b48-4649-a914-5cb2f9575bf3
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: PTRANSLATE_ADDRESS_ROUTINE, PTRANSLATE_ADDRESS_ROUTINE64, TranslateAddressProc64, TranslateAddressProc64 callback, TranslateAddressProc64 callback function, _win32_translateaddressproc64, base.translateaddressproc64, dbghelp/TranslateAddressProc64
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
 - TranslateAddressProc64
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# PTRANSLATE_ADDRESS_ROUTINE64 callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a> function. It provides address translation for 16-bit addresses.

The <b>PTRANSLATE_ADDRESS_ROUTINE64</b> type defines a pointer to this callback function. 
<b>TranslateAddressProc64</b> is a placeholder for the application-defined function name.


## -parameters




### -param hProcess [in]

A handle to the process for which the stack trace is generated.


### -param hThread [in]

A handle to the thread for which the stack trace is generated.


### -param lpaddr [in]

An address to be translated.


## -returns



The function returns the translated address.




## -remarks



This callback function supersedes the <i>PTRANSLATE_ADDRESS_ROUTINE</i> callback function.  <i>PTRANSLATE_ADDRESS_ROUTINE</i> is defined as follows in Dbghelp.h.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define PTRANSLATE_ADDRESS_ROUTINE PTRANSLATE_ADDRESS_ROUTINE64
#else
typedef
DWORD
(__stdcall *PTRANSLATE_ADDRESS_ROUTINE)(
    __in HANDLE hProcess,
    __in HANDLE hThread,
    __out LPADDRESS lpaddr
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a>
 

 

