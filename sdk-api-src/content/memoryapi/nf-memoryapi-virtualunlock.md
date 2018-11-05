---
UID: NF:memoryapi.VirtualUnlock
title: VirtualUnlock function
author: windows-sdk-content
description: Unlocks a specified range of pages in the virtual address space of a process, enabling the system to swap the pages out to the paging file if necessary.
old-location: base\virtualunlock.htm
tech.root: Memory
ms.assetid: cb868c8a-ac0d-42ad-bf72-2ae617bc0427
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: VirtualUnlock, VirtualUnlock function, _win32_virtualunlock, base.virtualunlock, winbase/VirtualUnlock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
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
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - VirtualUnlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VirtualUnlock function


## -description


Unlocks a specified range of pages in the virtual address space of a process, enabling the system to swap the pages out to the paging file if necessary.


## -parameters




### -param lpAddress [in]

A pointer to the base address of the region of pages to be unlocked.


### -param dwSize [in]

The size of the region being unlocked, in bytes. The region of affected pages includes all pages containing one or more bytes in the range from the <i>lpAddress</i> parameter to <code>(lpAddress+dwSize)</code>. This means that a 2-byte range straddling a page boundary causes both pages to be unlocked.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For the function to succeed, the range specified need not match a range passed to a previous call to the 
<a href="https://msdn.microsoft.com/414c4704-36f2-40f9-a69a-9d53ab354c30">VirtualLock</a> function, but all pages in the range must be locked. If any of the pages in the specified range are not locked, <b>VirtualUnlock</b> removes such pages from the working set, sets last error to <b>ERROR_NOT_LOCKED</b>, and returns <b>FALSE</b>.

Calling 
<b>VirtualUnlock</b> on a range of memory that is not locked releases the pages from the process's working set.




## -see-also




<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/9488a854-1ef0-488f-b3d1-57c1acb82a88">Virtual Memory Functions</a>



<a href="https://msdn.microsoft.com/414c4704-36f2-40f9-a69a-9d53ab354c30">VirtualLock</a>
 

 

