---
UID: NF:threadpoolapiset.WaitForThreadpoolWaitCallbacks
title: WaitForThreadpoolWaitCallbacks function
author: windows-driver-content
description: Waits for outstanding wait callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.
old-location: base\waitforthreadpoolwaitcallbacks.htm
old-project: ProcThread
ms.assetid: 49c40b35-a0ed-40a1-9c35-5d3985ebd98f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: WaitForThreadpoolWaitCallbacks, WaitForThreadpoolWaitCallbacks function, base.waitforthreadpoolwaitcallbacks, threadpoolapiset/WaitForThreadpoolWaitCallbacks, winbase/WaitForThreadpoolWaitCallbacks
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
-	WaitForThreadpoolWaitCallbacks
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# WaitForThreadpoolWaitCallbacks function


## -description


Waits for outstanding wait callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.


## -parameters




### -param pwa [in, out]

A <b>TP_WAIT</b> structure that defines the wait object. The <a href="https://msdn.microsoft.com/ba19f5f9-d4b0-4865-9609-95e7697d61c0">CreateThreadpoolWait</a> function returns the <b>TP_WAIT</b> structure.


### -param fCancelPendingCallbacks [in]

Indicates whether to cancel queued callbacks that have not yet started to execute.


## -returns



This function does not return a value.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f8323ad2-c0b6-4e5c-b6eb-7195673f8992">CloseThreadpoolWait</a>



<a href="https://msdn.microsoft.com/ba19f5f9-d4b0-4865-9609-95e7697d61c0">CreateThreadpoolWait</a>



<a href="https://msdn.microsoft.com/ebd0ecad-a864-43cf-a1cb-e4c2d595ef81">SetThreadpoolWait</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

