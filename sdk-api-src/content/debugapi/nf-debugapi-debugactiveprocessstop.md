---
UID: NF:debugapi.DebugActiveProcessStop
title: DebugActiveProcessStop function (debugapi.h)
author: windows-sdk-content
description: Stops the debugger from debugging the specified process.
old-location: base\debugactiveprocessstop.htm
tech.root: Debug
ms.assetid: 29d1a6d1-0c10-43c1-bef1-b063f07b16a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DebugActiveProcessStop, DebugActiveProcessStop function, _win32_debugactiveprocessstop, base.debugactiveprocessstop, debugapi/DebugActiveProcessStop
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
 - API-MS-Win-Core-debug-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Debug-L1-1-2.dll
api_name:
 - DebugActiveProcessStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DebugActiveProcessStop function


## -description


Stops the debugger from debugging the specified process.


## -parameters




### -param dwProcessId [in]

The identifier of the process to stop debugging.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/306a5b28-658a-4dab-a516-c638b73f4a77">DebugActiveProcess</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/2662411f-a69a-442b-a177-a27ea025bb01">Debugging a Running Process</a>



<a href="https://msdn.microsoft.com/7056e181-9bc5-4530-a7b8-d5ff1e345eef">Process Functions for Debugging</a>
 

 

