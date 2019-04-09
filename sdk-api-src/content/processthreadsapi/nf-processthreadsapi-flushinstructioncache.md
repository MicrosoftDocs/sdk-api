---
UID: NF:processthreadsapi.FlushInstructionCache
title: FlushInstructionCache function (processthreadsapi.h)
author: windows-sdk-content
description: Flushes the instruction cache for the specified process.
old-location: base\flushinstructioncache.htm
tech.root: Debug
ms.assetid: 6267adde-8169-4673-97ec-78c66e2135c1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FlushInstructionCache, FlushInstructionCache function, _win32_flushinstructioncache, base.flushinstructioncache, processthreadsapi/FlushInstructionCache
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - FlushInstructionCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FlushInstructionCache function


## -description


Flushes the instruction cache for the specified process.


## -parameters




### -param hProcess [in]

A handle to a process whose instruction cache is to be flushed.


### -param lpBaseAddress [in]

A pointer to the base of the region to be flushed. This parameter can be <b>NULL</b>.


### -param dwSize [in]

The size of the region to be flushed if the <i>lpBaseAddress</i> parameter is not <b>NULL</b>, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Applications should call 
<b>FlushInstructionCache</b> if they generate or modify code in memory. The CPU cannot detect the change, and may execute the old code it cached.




## -see-also




<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>
 

 

