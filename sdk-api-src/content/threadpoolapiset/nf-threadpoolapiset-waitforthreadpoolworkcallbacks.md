---
UID: NF:threadpoolapiset.WaitForThreadpoolWorkCallbacks
title: WaitForThreadpoolWorkCallbacks function
author: windows-driver-content
description: Waits for outstanding work callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.
old-location: base\waitforthreadpoolworkcallbacks.htm
old-project: ProcThread
ms.assetid: 97c16892-d6ef-4216-ac79-344e83ab35bc
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: WaitForThreadpoolWorkCallbacks, WaitForThreadpoolWorkCallbacks function, base.waitforthreadpoolworkcallbacks, threadpoolapiset/WaitForThreadpoolWorkCallbacks, winbase/WaitForThreadpoolWorkCallbacks
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: threadpoolapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TS_TEXTCHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-threadpool-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-threadpool-l1-2-0.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	WaitForThreadpoolWorkCallbacks
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# WaitForThreadpoolWorkCallbacks function


## -description


Waits for outstanding work callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.


## -parameters




### -param pwk [in, out]

A <b>TP_WORK</b> structure that defines the work object. The <a href="https://msdn.microsoft.com/50647d87-1768-4918-8376-a6a04daca621">CreateThreadpoolWork</a> function returns this structure.


### -param fCancelPendingCallbacks [in]

Indicates whether to cancel queued callbacks that have not yet started to execute.


## -returns



This function does not return a value.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/89d7362e-0814-4f7e-a27f-8a297e210559">CloseThreadpoolWork</a>



<a href="https://msdn.microsoft.com/50647d87-1768-4918-8376-a6a04daca621">CreateThreadpoolWork</a>



<a href="https://msdn.microsoft.com/28df173d-b78c-4158-97d5-63117a2d3967">SubmitThreadpoolWork</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

