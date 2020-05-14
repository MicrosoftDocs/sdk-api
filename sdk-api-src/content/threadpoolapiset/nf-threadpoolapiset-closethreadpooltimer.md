---
UID: NF:threadpoolapiset.CloseThreadpoolTimer
title: CloseThreadpoolTimer function (threadpoolapiset.h)
description: Releases the specified timer object.helpviewer_keywords: ["CloseThreadpoolTimer","CloseThreadpoolTimer function","base.closethreadpooltimer","threadpoolapiset/CloseThreadpoolTimer","winbase/CloseThreadpoolTimer"]
old-location: base\closethreadpooltimer.htm
tech.root: ProcThread
ms.assetid: c1270c5d-a1f5-4481-a343-c1ff3301a56e
ms.date: 12/05/2018
ms.keywords: CloseThreadpoolTimer, CloseThreadpoolTimer function, base.closethreadpooltimer, threadpoolapiset/CloseThreadpoolTimer, winbase/CloseThreadpoolTimer
f1_keywords:
- threadpoolapiset/CloseThreadpoolTimer
dev_langs:
- c++
req.header: threadpoolapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-l1-2-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
api_name:
- CloseThreadpoolTimer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CloseThreadpoolTimer function


## -description


Releases the specified timer object.


## -parameters




### -param pti [in, out]

A <b>TP_TIMER</b> structure that defines the timer object. The <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a> function returns this structure.


## -remarks



The timer object is freed immediately if there are no outstanding callbacks; otherwise, the timer object is freed asynchronously after the outstanding callback functions complete. 

In some cases, callback functions might run after <b>CloseThreadpoolTimer</b> has been called. To prevent this behavior: 

<ol>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer">SetThreadpoolTimer</a> function with the <i>pftDueTime</i> parameter set to NULL and the <i>msPeriod</i> and <i>msWindowLength</i> parameters set to 0. </li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks">WaitForThreadpoolTimerCallbacks</a> function.</li>
<li>Call <b>CloseThreadpoolTimer</b>.</li>
</ol>
If there is a cleanup group associated with the timer object, it is not necessary to call this function; calling the <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a> function releases the  work, wait, and timer objects associated with the cleanup group.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset">IsThreadpoolTimerSet</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer">SetThreadpoolTimer</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks">WaitForThreadpoolTimerCallbacks</a>
 

 

