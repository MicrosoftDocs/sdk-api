---
UID: NF:winbase.ConvertFiberToThread
title: ConvertFiberToThread function
author: windows-driver-content
description: Converts the current fiber into a thread.
old-location: base\convertfibertothread.htm
old-project: ProcThread
ms.assetid: 194c5289-0d25-4ce1-9c32-9e87b12db825
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ConvertFiberToThread, ConvertFiberToThread function, _win32_convertfibertothread, base.convertfibertothread, winbase/ConvertFiberToThread
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ConvertFiberToThread
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ConvertFiberToThread function


## -description


Converts the current fiber into a thread.


## -parameters






## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The function releases the resources allocated by the 
<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a> function. After calling this function, you cannot call any of the fiber functions from the thread.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a>



<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

