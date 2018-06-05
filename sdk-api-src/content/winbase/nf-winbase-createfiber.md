---
UID: NF:winbase.CreateFiber
title: CreateFiber function
author: windows-sdk-content
description: Allocates a fiber object, assigns it a stack, and sets up execution to begin at the specified start address, typically the fiber function. This function does not schedule the fiber.
old-location: base\createfiber.htm
old-project: ProcThread
ms.assetid: 3e44776b-7ef2-43fb-a2ae-e8ab7e20644b
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: CreateFiber, CreateFiber function, _win32_createfiber, base.createfiber, winbase/CreateFiber
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-fibers-l2-1-0.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-fibers-l2-1-1.dll
-	API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
-	KernelBase.dll
api_name:
-	CreateFiber
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateFiber function


## -description


Allocates a fiber object, assigns it a stack, and sets up execution to begin at the specified start address, typically the fiber function. This function does not schedule the fiber.

To specify both a commit and reserve stack size, use the 
<a href="https://msdn.microsoft.com/eb27cfcf-6086-47df-a5b4-93c51a5e1577">CreateFiberEx</a> function.


## -parameters




### -param dwStackSize [in]

The initial size of the stack, in bytes. If this parameter is zero, the new fiber uses the default stack size for the executable. For more information, see <a href="https://msdn.microsoft.com/abb2d5c1-040b-4c36-aae5-3517b6a8c540">Thread Stack Size</a>.


### -param lpStartAddress [in]

A pointer to the application-defined function to be executed by the fiber and represents the starting address of the fiber. Execution of the newly created fiber does not begin until another fiber calls the 
<a href="https://msdn.microsoft.com/020a8c97-848d-4b33-9cfb-77e5bff644fd">SwitchToFiber</a> function with this address. For more information of the fiber callback function, see 
<a href="https://msdn.microsoft.com/368d98f3-1ecd-47a0-98cc-0636f055ae41">FiberProc</a>.


### -param lpParameter [in, optional]

A pointer to a variable that is passed to the fiber. The fiber can retrieve this data by using the 
<a href="https://msdn.microsoft.com/72e616ce-4188-4944-b627-9681e5fd271e">GetFiberData</a> macro.


## -returns



If the function succeeds, the return value is the address of the fiber.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The number of fibers a process can create is limited by the available virtual memory. For example, if you create each fiber with 1 megabyte of reserved stack space, you can create at most 2028 fibers. If you reduce the default stack size by using the STACKSIZE statement in the module definition (.def) file or 
by using <a href="https://msdn.microsoft.com/eb27cfcf-6086-47df-a5b4-93c51a5e1577">CreateFiberEx</a>, you can create more fibers. However, your application will have better performance if you use an alternate strategy for processing requests instead of creating such a large number of fibers.

Before a thread can schedule a fiber using the 
<a href="https://msdn.microsoft.com/020a8c97-848d-4b33-9cfb-77e5bff644fd">SwitchToFiber</a> function, it must call the 
<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a> function so there is a fiber associated with the thread.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/b09c00ae-a498-499b-ba2b-735028e9fd8f">Using Fibers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a>



<a href="https://msdn.microsoft.com/eb27cfcf-6086-47df-a5b4-93c51a5e1577">CreateFiberEx</a>



<a href="https://msdn.microsoft.com/368d98f3-1ecd-47a0-98cc-0636f055ae41">FiberProc</a>



<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/72e616ce-4188-4944-b627-9681e5fd271e">GetFiberData</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/020a8c97-848d-4b33-9cfb-77e5bff644fd">SwitchToFiber</a>
 

 

