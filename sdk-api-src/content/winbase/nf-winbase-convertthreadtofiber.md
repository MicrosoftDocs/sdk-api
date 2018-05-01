---
UID: NF:winbase.ConvertThreadToFiber
title: ConvertThreadToFiber function
author: windows-driver-content
description: Converts the current thread into a fiber. You must convert a thread into a fiber before you can schedule other fibers.
old-location: base\convertthreadtofiber.htm
old-project: ProcThread
ms.assetid: 31954a7e-b9a3-4d60-b43a-54fe0047f380
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: ConvertThreadToFiber, ConvertThreadToFiber function, _win32_convertthreadtofiber, base.convertthreadtofiber, winbase/ConvertThreadToFiber
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ConvertThreadToFiber
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ConvertThreadToFiber function


## -description


Converts the current thread into a fiber. You must convert a thread into a fiber before you can schedule other fibers.


## -parameters




### -param lpParameter [in, optional]

A pointer to a variable that is passed to the fiber. The fiber can retrieve this data by using the 
<a href="https://msdn.microsoft.com/72e616ce-4188-4944-b627-9681e5fd271e">GetFiberData</a> macro.


## -returns



If the function succeeds, the return value is the address of the fiber.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Only fibers can execute other fibers. If a thread needs to execute a fiber, it must call 
<b>ConvertThreadToFiber</b> or 
<a href="https://msdn.microsoft.com/cb0473f8-bc49-44c9-a8b7-6d5b55aa37a5">ConvertThreadToFiberEx</a> to create an area in which to save fiber state information. The thread is now the current fiber. The state information for this fiber includes the fiber data specified by <i>lpParameter</i>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/b09c00ae-a498-499b-ba2b-735028e9fd8f">Using Fibers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/194c5289-0d25-4ce1-9c32-9e87b12db825">ConvertFiberToThread</a>



<a href="https://msdn.microsoft.com/cb0473f8-bc49-44c9-a8b7-6d5b55aa37a5">ConvertThreadToFiberEx</a>



<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/72e616ce-4188-4944-b627-9681e5fd271e">GetFiberData</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

