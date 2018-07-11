---
UID: NF:winbase.LocalFree
title: LocalFree function
author: windows-sdk-content
description: Frees the specified local memory object and invalidates its handle.
old-location: base\localfree.htm
old-project: memory
ms.assetid: a0393983-cb43-4dfa-91a6-d82a5fb8de12
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: LocalFree, LocalFree function, _win32_localfree, base.localfree, winbase/LocalFree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Heap-l2-1-0.dll
api_name:
 - LocalFree
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LocalFree function


## -description


Frees the specified local memory object and invalidates its handle.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.</div><div> </div>

## -parameters




### -param hMem [in]

A handle to the local memory object. This handle is returned by either the 
<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> or 
<a href="https://msdn.microsoft.com/88527ddd-e0c2-4a41-825e-d3a6df77fd2a">LocalReAlloc</a> function. It is not safe to free memory allocated with <a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>.


## -returns



If the function succeeds, the return value is <b>NULL</b>.

If the function fails, the return value is equal to a handle to the local memory object. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the process tries to examine or modify the memory after it has been freed, heap corruption may occur or an access violation exception (EXCEPTION_ACCESS_VIOLATION) may be generated.

If the <i>hMem</i> parameter is <b>NULL</b>, 
<b>LocalFree</b> ignores the parameter and returns <b>NULL</b>.

The 
<b>LocalFree</b> function will free a locked memory object. A locked memory object has a lock count greater than zero. The 
<a href="https://msdn.microsoft.com/a9432e28-9fbd-4a7e-8dce-fad3da04804a">LocalLock</a> function locks a local memory object and increments the lock count by one. The 
<a href="https://msdn.microsoft.com/eac40b69-5fb6-4523-826d-a012f6f4e5ce">LocalUnlock</a> function unlocks it and decrements the lock count by one. To get the lock count of a local memory object, use the 
<a href="https://msdn.microsoft.com/4804c8c3-6c0b-4f62-87ab-f64b23fff8b9">LocalFlags</a> function.

If an application is running under a debug version of the system, 
<b>LocalFree</b> will issue a message that tells you that a locked object is being freed. If you are debugging the application, 
<b>LocalFree</b> will enter a breakpoint just before freeing a locked object. This allows you to verify the intended behavior, then continue execution.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a>



<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>



<a href="https://msdn.microsoft.com/4804c8c3-6c0b-4f62-87ab-f64b23fff8b9">LocalFlags</a>



<a href="https://msdn.microsoft.com/a9432e28-9fbd-4a7e-8dce-fad3da04804a">LocalLock</a>



<a href="https://msdn.microsoft.com/88527ddd-e0c2-4a41-825e-d3a6df77fd2a">LocalReAlloc</a>



<a href="https://msdn.microsoft.com/eac40b69-5fb6-4523-826d-a012f6f4e5ce">LocalUnlock</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
		  Management Functions</a>
 

 

