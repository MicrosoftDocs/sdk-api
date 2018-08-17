---
UID: NF:winbase.DebugBreakProcess
title: DebugBreakProcess function
author: windows-sdk-content
description: Causes a breakpoint exception to occur in the specified process. This allows the calling thread to signal the debugger to handle the exception.
old-location: base\debugbreakprocess.htm
old-project: debug
ms.assetid: db90d46b-fdbc-49c9-ac99-6b1db1db708c
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: DebugBreakProcess, DebugBreakProcess function, _win32_debugbreakprocess, base.debugbreakprocess, winbase/DebugBreakProcess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - DebugBreakProcess
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DebugBreakProcess function


## -description


Causes a breakpoint exception to occur in the specified process. This allows the calling thread to signal the debugger to handle the exception.


## -parameters




### -param Process [in]

A handle to the process.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the process is not being debugged, the function uses the search logic of a standard exception handler. In most cases, this causes the process to terminate because of an unhandled breakpoint exception.




## -see-also




<a href="https://msdn.microsoft.com/d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f">Communicating with the Debugger</a>



<a href="https://msdn.microsoft.com/1ca9d2d1-eed4-4982-8964-64b44e8be256">DebugBreak</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>
 

 

