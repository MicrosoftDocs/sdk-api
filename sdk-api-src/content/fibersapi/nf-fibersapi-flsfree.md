---
UID: NF:fibersapi.FlsFree
title: FlsFree function
author: windows-sdk-content
description: Releases a fiber local storage (FLS) index, making it available for reuse.
old-location: base\flsfree.htm
tech.root: ProcThread
ms.assetid: ef996c6b-77d0-4b06-97a4-14773cb67146
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FlsFree, FlsFree function, _win32_flsfree, base.flsfree, fibersapi/FlsFree, winbase/FlsFree
ms.topic: function
f1_keywords: 
 - "fibersapi/FlsFree"
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
 - FlsFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FlsFree function


## -description


Releases a fiber local storage (FLS) index, making it available for reuse.


## -parameters




### -param dwFlsIndex [in]

The FLS index that was allocated by the 
<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Freeing an FLS index frees the index for all instances of FLS in the current process. Freeing an FLS index also causes the associated callback routine to be called for each fiber, if the corresponding FLS slot contains a non-NULL value.

If the fibers of the process have allocated memory and stored a pointer to the memory in an FLS slot, they should free the memory before calling 
<b>FlsFree</b>. The 
<b>FlsFree</b> function does not free memory blocks whose addresses have been stored in the FLS slots associated with the FLS index. It is expected that DLLs call this function (if at all) only during DLL_PROCESS_DETACH.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
 

 

