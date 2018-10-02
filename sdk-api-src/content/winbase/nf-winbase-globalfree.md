---
UID: NF:winbase.GlobalFree
title: GlobalFree function
author: windows-sdk-content
description: Frees the specified global memory object and invalidates its handle.
old-location: base\globalfree.htm
tech.root: Memory
ms.assetid: 5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GlobalFree, GlobalFree function, _win32_globalfree, base.globalfree, winbase/GlobalFree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
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
 - API-MS-Win-Core-Heap-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-Ms-Win-Core-Heap-L2-1-0.dll
api_name:
 - GlobalFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GlobalFree function


## -description


Frees the specified global memory object and invalidates its handle.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.
</div><div> </div>

## -parameters




### -param hMem [in]

A handle to the global memory object. This handle is returned by either the 
<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> or 
<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> function. It is not safe to free memory allocated with <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>.


## -returns



If the function succeeds, the return value is <b>NULL</b>.

If the function fails, the return value is equal to a handle to the global memory object. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the process examines or modifies the memory after it has been freed, heap corruption may occur or an access violation exception (EXCEPTION_ACCESS_VIOLATION) may be generated.

The 
<b>GlobalFree</b> function will free a locked memory object. A locked memory object has a lock count greater than zero. The 
<a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a> function locks a global memory object and increments the lock count by one. The 
<a href="https://msdn.microsoft.com/580a2873-7f06-47a1-acf5-c2b3c96e15e7">GlobalUnlock</a> function unlocks it and decrements the lock count by one. To get the lock count of a global memory object, use the 
<a href="https://msdn.microsoft.com/647fc9a2-0522-42ab-ab8b-43c648f27d90">GlobalFlags</a> function.

If an application is running under a debug version of the system, 
<b>GlobalFree</b> will issue a message that tells you that a locked object is being freed. If you are debugging the application, 
<b>GlobalFree</b> will enter a breakpoint just before freeing a locked object. This allows you to verify the intended behavior, then continue execution.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>



<a href="https://msdn.microsoft.com/647fc9a2-0522-42ab-ab8b-43c648f27d90">GlobalFlags</a>



<a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a>



<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a>



<a href="https://msdn.microsoft.com/580a2873-7f06-47a1-acf5-c2b3c96e15e7">GlobalUnlock</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
		  Management Functions</a>
 

 

