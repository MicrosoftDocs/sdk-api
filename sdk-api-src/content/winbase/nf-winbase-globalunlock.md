---
UID: NF:winbase.GlobalUnlock
title: GlobalUnlock function
author: windows-sdk-content
description: Decrements the lock count associated with a memory object that was allocated with GMEM_MOVEABLE.
old-location: base\globalunlock.htm
old-project: memory
ms.assetid: 580a2873-7f06-47a1-acf5-c2b3c96e15e7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GlobalUnlock, GlobalUnlock function, _win32_globalunlock, base.globalunlock, winbase/GlobalUnlock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Heap-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
api_name:
 - GlobalUnlock
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GlobalUnlock function


## -description


Decrements the lock count associated with a memory object that was allocated with <b>GMEM_MOVEABLE</b>. This function has no effect on memory objects allocated with <b>GMEM_FIXED</b>.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.
</div><div> </div>

## -parameters




### -param hMem [in]

A handle to the global memory object. This handle is returned by either the 
<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> or 
<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> function.


## -returns



If the memory object is still locked after decrementing the lock count, the return value is a nonzero value. If the memory object is unlocked after decrementing the lock count, the function returns zero and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>NO_ERROR</b>.

If the function fails, the return value is zero and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns a value other than <b>NO_ERROR</b>.




## -remarks



The internal data structures for each memory object include a lock count that is initially zero. For movable memory objects, the 
<a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a> function increments the count by one, and 
<b>GlobalUnlock</b> decrements the count by one. For each call that a process makes to 
<b>GlobalLock</b> for an object, it must eventually call 
<b>GlobalUnlock</b>. Locked memory will not be moved or discarded, unless the memory object is reallocated by using the 
<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> function. The memory block of a locked memory object remains locked until its lock count is decremented to zero, at which time it can be moved or discarded.

Memory objects allocated with <b>GMEM_FIXED</b> always have a lock count of zero. If the specified memory block is fixed memory, this function returns <b>TRUE</b>.

If the memory object is already unlocked, 
<b>GlobalUnlock</b> returns <b>FALSE</b> and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> reports <b>ERROR_NOT_LOCKED</b>.

A process should not rely on the return value to determine the number of times it must subsequently call 
<b>GlobalUnlock</b> for a memory object.




## -see-also




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>



<a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a>



<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>
 

 

