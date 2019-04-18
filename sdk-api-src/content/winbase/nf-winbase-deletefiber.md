---
UID: NF:winbase.DeleteFiber
title: DeleteFiber function (winbase.h)
author: windows-sdk-content
description: Deletes an existing fiber.
old-location: base\deletefiber.htm
tech.root: ProcThread
ms.assetid: e1a7453a-6878-49dd-831f-1857a489e97f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteFiber, DeleteFiber function, _win32_deletefiber, base.deletefiber, winbase/DeleteFiber
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
 - API-MS-Win-Core-fibers-l2-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-fibers-l2-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - KernelBase.dll
api_name:
 - DeleteFiber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteFiber function


## -description


Deletes an existing fiber.


## -parameters




### -param lpFiber [in]

The address of the fiber to be deleted.


## -returns



This function does not return a value.




## -remarks



The 
<b>DeleteFiber</b> function deletes all data associated with the fiber. This data includes the stack, a subset of the registers, and the fiber data.

If the currently running fiber calls 
<b>DeleteFiber</b>, its thread calls 
<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> and terminates. However, if a currently running fiber is deleted by another fiber, the thread running the deleted fiber is likely to terminate abnormally because the fiber stack has been freed.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/b09c00ae-a498-499b-ba2b-735028e9fd8f">Using Fibers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a>



<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

