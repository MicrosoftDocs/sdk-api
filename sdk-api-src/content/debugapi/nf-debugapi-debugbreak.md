---
UID: NF:debugapi.DebugBreak
title: DebugBreak function (debugapi.h)
author: windows-sdk-content
description: Causes a breakpoint exception to occur in the current process. This allows the calling thread to signal the debugger to handle the exception.
old-location: base\debugbreak.htm
tech.root: Debug
ms.assetid: 1ca9d2d1-eed4-4982-8964-64b44e8be256
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DebugBreak, DebugBreak function, _win32_debugbreak, base.debugbreak, debugapi/DebugBreak
ms.topic: function
req.header: debugapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - API-MS-Win-Core-debug-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-debug-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Debug-L1-1-2.dll
api_name:
 - DebugBreak
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DebugBreak function


## -description


Causes a breakpoint exception to occur in the current process. This allows the calling thread to signal the debugger to handle the exception.

To cause a breakpoint exception in another process, use the 
<a href="https://msdn.microsoft.com/db90d46b-fdbc-49c9-ac99-6b1db1db708c">DebugBreakProcess</a> function.


## -parameters






## -returns



This function does not return a value.




## -remarks



If the process is not being debugged, the function uses the search logic of a standard exception handler. In most cases, this causes the calling process to terminate because of an unhandled breakpoint exception.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/c3b4e696-9f45-4616-ac6b-07ba29750bb2">Using an Exception Handler</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f">Communicating with the Debugger</a>



<a href="https://msdn.microsoft.com/306a5b28-658a-4dab-a516-c638b73f4a77">DebugActiveProcess</a>



<a href="https://msdn.microsoft.com/db90d46b-fdbc-49c9-ac99-6b1db1db708c">DebugBreakProcess</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>
 

 

