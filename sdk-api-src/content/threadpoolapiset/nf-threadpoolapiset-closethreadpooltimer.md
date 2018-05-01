---
UID: NF:threadpoolapiset.CloseThreadpoolTimer
title: CloseThreadpoolTimer function
author: windows-driver-content
description: Releases the specified timer object.
old-location: base\closethreadpooltimer.htm
old-project: ProcThread
ms.assetid: c1270c5d-a1f5-4481-a343-c1ff3301a56e
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: CloseThreadpoolTimer, CloseThreadpoolTimer function, base.closethreadpooltimer, threadpoolapiset/CloseThreadpoolTimer, winbase/CloseThreadpoolTimer
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
-	CloseThreadpoolTimer
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CloseThreadpoolTimer function


## -description


Releases the specified timer object.


## -parameters




### -param pti [in, out]

A <b>TP_TIMER</b> structure that defines the timer object. The <a href="https://msdn.microsoft.com/1fa98b79-e646-4e48-9979-1817d2c1b713">CreateThreadpoolTimer</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



The timer object is freed immediately if there are no outstanding callbacks; otherwise, the timer object is freed asynchronously after the outstanding callback functions complete. 

In some cases, callback functions might run after <b>CloseThreadpoolTimer</b> has been called. To prevent this behavior: 

<ol>
<li>Call the <a href="https://msdn.microsoft.com/017f88c6-e14c-47ba-94d2-e7bb0dc95d12">SetThreadpoolTimer</a> function with the <i>pftDueTime</i> parameter set to NULL and the <i>msPeriod</i> and <i>msWindowLength</i> parameters set to 0. </li>
<li>Call the <a href="https://msdn.microsoft.com/511488b8-9e92-47b9-8b3c-7ece9d9f996c">WaitForThreadpoolTimerCallbacks</a> function.</li>
<li>Call <b>CloseThreadpoolTimer</b>.</li>
</ol>
If there is a cleanup group associated with the timer object, it is not necessary to call this function; calling the <a href="https://msdn.microsoft.com/9c78db13-d8dd-4eda-83d9-c9dbbfc6e822">CloseThreadpoolCleanupGroupMembers</a> function releases the  work, wait, and timer objects associated with the cleanup group.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/1fa98b79-e646-4e48-9979-1817d2c1b713">CreateThreadpoolTimer</a>



<a href="https://msdn.microsoft.com/f9dee0aa-6310-4218-b207-72a24c5019e2">IsThreadpoolTimerSet</a>



<a href="https://msdn.microsoft.com/017f88c6-e14c-47ba-94d2-e7bb0dc95d12">SetThreadpoolTimer</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/511488b8-9e92-47b9-8b3c-7ece9d9f996c">WaitForThreadpoolTimerCallbacks</a>
 

 

