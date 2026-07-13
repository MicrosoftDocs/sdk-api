---
UID: NF:threadpoolapiset.SetThreadpoolTimer
title: SetThreadpoolTimer function (threadpoolapiset.h)
description: Sets the timer object, replacing the previous timer, if any. A worker thread calls the timer object's callback after the specified timeout expires. (SetThreadpoolTimer)
helpviewer_keywords: ["SetThreadpoolTimer","SetThreadpoolTimer function","base.setthreadpooltimer","threadpoolapiset/SetThreadpoolTimer","winbase/SetThreadpoolTimer"]
old-location: base\setthreadpooltimer.htm
tech.root: backup
ms.assetid: 017f88c6-e14c-47ba-94d2-e7bb0dc95d12
ms.date: 12/05/2018
ms.keywords: SetThreadpoolTimer, SetThreadpoolTimer function, base.setthreadpooltimer, threadpoolapiset/SetThreadpoolTimer, winbase/SetThreadpoolTimer
req.header: threadpoolapiset.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadpoolTimer
 - threadpoolapiset/SetThreadpoolTimer
dev_langs:
 - c++
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
 - SetThreadpoolTimer
---

# SetThreadpoolTimer function


## -description

Sets the timer object, replacing the previous timer, if any. A worker thread calls the timer object's callback after the specified timeout expires.

## -parameters

### -param pti [in, out]

A pointer to a <b>TP_TIMER</b> structure that defines the timer object to set. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a> function returns this pointer.

### -param pftDueTime [in, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the absolute or relative time at which the timer should expire.  If positive or zero, it indicates the absolute time since January 1, 1601 (UTC), measured in 100 nanosecond units. If negative, it indicates the amount of time to wait relative to the current time. For more information about time values, see <a href="/windows/desktop/SysInfo/file-times">File Times</a>.

If this parameter is NULL, the timer object will cease to queue new callbacks (but callbacks already queued will still occur).

The timer is set if the <i>pftDueTime</i> parameter is non-NULL.

### -param msPeriod [in]

The timer period, in milliseconds. If this parameter is zero, the timer is signaled once. If this parameter is greater than zero, the timer is periodic. A periodic timer automatically reactivates each time the period elapses, until the timer is canceled.

### -param msWindowLength [in]

The maximum amount of time the system can delay before calling the timer callback. If this parameter is not set to zero, the system can batch calls to conserve power.

## -remarks

Setting the timer cancels the previous timer, if any.

In some cases, callback functions might run after an application closes the threadpool timer. To prevent this behavior, an application should follow the steps described in <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer">CloseThreadpoolTimer</a>.

If the due time specified by <i>pftDueTime</i> is relative, the time that the system spends in sleep or hibernation does not count toward the expiration of the timer. The timer is signaled when the cumulative amount of elapsed time the system spends in the waking state equals the timer's relative due time or period. If the  due time specified by <i>pftDueTime</i> is absolute, the time that the system spends in sleep or hibernation does count toward the expiration of the timer. If the timer expires while the system is sleeping, the timer is signaled immediately when the system wakes.

If the due time specified by <i>pftDueTime</i> is zero, then the timer expires immediately.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer">CloseThreadpoolTimer</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset">IsThreadpoolTimerSet</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks">WaitForThreadpoolTimerCallbacks</a>
