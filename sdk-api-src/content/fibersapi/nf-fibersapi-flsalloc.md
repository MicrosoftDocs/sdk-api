---
UID: NF:fibersapi.FlsAlloc
title: FlsAlloc function

description: Allocates a fiber local storage (FLS) index.
old-location: base\flsalloc.htm
tech.root: ProcThread
ms.assetid: dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59

ms.date: 12/05/2018
ms.keywords: FlsAlloc, FlsAlloc function, _win32_flsalloc, base.flsalloc, fibersapi/FlsAlloc, winbase/FlsAlloc
ms.topic: function
f1_keywords: 
 - "fibersapi/FlsAlloc"
dev_langs:
 - c++
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
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nc-winnt-pfls_callback_function">FlsCallback</a>.


## -returns



If the function succeeds, the return value is an FLS index initialized to zero.

If the function fails, the return value is FLS_OUT_OF_INDEXES. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The fibers of the process can use the FLS index in subsequent calls to the 
<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flsfree">FlsFree</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flssetvalue">FlsSetValue</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flsgetvalue">FlsGetValue</a> functions.

FLS indexes are typically allocated during process or dynamic-link library (DLL) initialization. After an FLS index has been allocated, each fiber of the process can use it to access its own FLS storage slot. To store a value in its FLS slot, a fiber specifies the index in a call to 
<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flssetvalue">FlsSetValue</a>. The fiber specifies the same index in a subsequent call to 
<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flsgetvalue">FlsGetValue</a> to retrieve the stored value.

FLS indexes are not valid across process boundaries. A DLL cannot assume that an index assigned in one process is valid in another process.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nc-winnt-pfls_callback_function">FlsCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flsfree">FlsFree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flsgetvalue">FlsGetValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flssetvalue">FlsSetValue</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
 

 

