---
UID: NF:fibersapi.FlsAlloc
title: FlsAlloc function
author: windows-sdk-content
description: Allocates a fiber local storage (FLS) index.
old-location: base\flsalloc.htm
tech.root: ProcThread
ms.assetid: dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FlsAlloc, FlsAlloc function, _win32_flsalloc, base.flsalloc, fibersapi/FlsAlloc, winbase/FlsAlloc
ms.topic: function
req.header: fibersapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-fibers-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-fibers-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FlsAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FlsAlloc function


## -description


Allocates a fiber local storage (FLS) index. Any fiber in the process can subsequently use this index to store and retrieve values that are local to the fiber.


## -parameters




### -param lpCallback [in]

A pointer to the application-defined callback function of type <b>PFLS_CALLBACK_FUNCTION</b>. This parameter is optional. For more information, see 
<a href="https://msdn.microsoft.com/d05a6550-7fec-44e6-9b38-dfafff7895c8">FlsCallback</a>.


## -returns



If the function succeeds, the return value is an FLS index initialized to zero.

If the function fails, the return value is FLS_OUT_OF_INDEXES. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The fibers of the process can use the FLS index in subsequent calls to the 
<a href="https://msdn.microsoft.com/ef996c6b-77d0-4b06-97a4-14773cb67146">FlsFree</a>, 
<a href="https://msdn.microsoft.com/f2abea00-8c1b-47e8-a4e9-9e3e7242d0ad">FlsSetValue</a>, or 
<a href="https://msdn.microsoft.com/5d5a1fe6-10ed-42c5-87db-b24eef6f174c">FlsGetValue</a> functions.

FLS indexes are typically allocated during process or dynamic-link library (DLL) initialization. After an FLS index has been allocated, each fiber of the process can use it to access its own FLS storage slot. To store a value in its FLS slot, a fiber specifies the index in a call to 
<a href="https://msdn.microsoft.com/f2abea00-8c1b-47e8-a4e9-9e3e7242d0ad">FlsSetValue</a>. The fiber specifies the same index in a subsequent call to 
<a href="https://msdn.microsoft.com/5d5a1fe6-10ed-42c5-87db-b24eef6f174c">FlsGetValue</a> to retrieve the stored value.

FLS indexes are not valid across process boundaries. A DLL cannot assume that an index assigned in one process is valid in another process.




## -see-also




<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/d05a6550-7fec-44e6-9b38-dfafff7895c8">FlsCallback</a>



<a href="https://msdn.microsoft.com/ef996c6b-77d0-4b06-97a4-14773cb67146">FlsFree</a>



<a href="https://msdn.microsoft.com/5d5a1fe6-10ed-42c5-87db-b24eef6f174c">FlsGetValue</a>



<a href="https://msdn.microsoft.com/f2abea00-8c1b-47e8-a4e9-9e3e7242d0ad">FlsSetValue</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

