---
UID: NF:winbase.CreateFiberEx
title: CreateFiberEx function
author: windows-sdk-content
description: Allocates a fiber object, assigns it a stack, and sets up execution to begin at the specified start address, typically the fiber function. This function does not schedule the fiber.
old-location: base\createfiberex.htm
tech.root: procthread
ms.assetid: eb27cfcf-6086-47df-a5b4-93c51a5e1577
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: CreateFiberEx, CreateFiberEx function, _win32_createfiberex, base.createfiberex, winbase/CreateFiberEx
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
 - API-MS-Win-Core-fibers-l2-1-1.dll
 - kernel32legacy.dll
 - KernelBase.dll
api_name:
 - CreateFiberEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateFiberEx function


## -description


Allocates a fiber object, assigns it a stack, and sets up execution to begin at the specified start address, typically the fiber function. This function does not schedule the fiber.


## -parameters




### -param dwStackCommitSize [in]

The initial commit size of the stack, in bytes. If this parameter is zero, the new fiber uses the default commit stack size for the executable. For more information, see <a href="https://msdn.microsoft.com/abb2d5c1-040b-4c36-aae5-3517b6a8c540">Thread Stack Size</a>.


### -param dwStackReserveSize [in]

The initial reserve size of the stack, in bytes. If this parameter is zero, the new fiber uses the default reserved stack size for the executable. For more information, see <a href="https://msdn.microsoft.com/abb2d5c1-040b-4c36-aae5-3517b6a8c540">Thread Stack Size</a>.


### -param dwFlags [in]

If this parameter is zero, the floating-point state on x86 systems is not switched and data can be corrupted if a fiber uses floating-point arithmetic. If this parameter is <b>FIBER_FLAG_FLOAT_SWITCH</b>, the floating-point state is switched for the fiber.

<b>Windows XP:  </b>The <b>FIBER_FLAG_FLOAT_SWITCH</b> flag is not supported.


### -param lpStartAddress [in]

A pointer to the application-defined function to be executed by the fiber and represents the starting address of the fiber. Execution of the newly created fiber does not begin until another fiber calls the 
<a href="https://msdn.microsoft.com/020a8c97-848d-4b33-9cfb-77e5bff644fd">SwitchToFiber</a> function with this address. For more information on the fiber callback function, see 
<a href="https://msdn.microsoft.com/368d98f3-1ecd-47a0-98cc-0636f055ae41">FiberProc</a>.


### -param lpParameter [in, optional]

A pointer to a variable that is passed to the fiber. The fiber can retrieve this data by using the 
<a href="https://msdn.microsoft.com/72e616ce-4188-4944-b627-9681e5fd271e">GetFiberData</a> macro.


## -returns



If the function succeeds, the return value is the address of the fiber.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The number of fibers a process can create is limited by the available virtual memory. By default, every fiber has 1 megabyte of reserved stack space. Therefore, you can create at most 2028 fibers. If you reduce the default stack size, you can create more fibers. However, your application will have better performance if you use an alternate strategy for processing requests.

Before a thread can schedule a fiber using the 
<a href="https://msdn.microsoft.com/020a8c97-848d-4b33-9cfb-77e5bff644fd">SwitchToFiber</a> function, it must call the 
<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a> function so there is a fiber associated with the thread.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a>



<a href="https://msdn.microsoft.com/368d98f3-1ecd-47a0-98cc-0636f055ae41">FiberProc</a>



<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/72e616ce-4188-4944-b627-9681e5fd271e">GetFiberData</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/020a8c97-848d-4b33-9cfb-77e5bff644fd">SwitchToFiber</a>
 

 

