---
UID: NF:threadpoolapiset.SetThreadpoolTimer
title: SetThreadpoolTimer function
author: windows-sdk-content
description: Sets the timer object&#8212;, replacing the previous timer, if any. A worker thread calls the timer object's callback after the specified timeout expires.
old-location: base\setthreadpooltimer.htm
tech.root: ProcThread
ms.assetid: 017f88c6-e14c-47ba-94d2-e7bb0dc95d12
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetThreadpoolTimer, SetThreadpoolTimer function, base.setthreadpooltimer, threadpoolapiset/SetThreadpoolTimer, winbase/SetThreadpoolTimer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - SetThreadpoolTimer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetThreadpoolTimer function


## -description


Sets the timer object—, replacing the previous timer, if any. A worker thread calls the timer object's callback after the specified timeout expires.


## -parameters




### -param pti [in, out]

A pointer to a <b>TP_TIMER</b> structure that defines the timer object to set. The <a href="https://msdn.microsoft.com/1fa98b79-e646-4e48-9979-1817d2c1b713">CreateThreadpoolTimer</a> function returns this structure.


### -param pftDueTime [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that specifies the absolute or relative time at which the timer should expire.  If positive or zero, it indicates the absolute time since January 1, 1601 (UTC), measured in 100 nanosecond units. If negative, it indicates the amount of time to wait relative to the current time. For more information about time values, see <a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>.

If this parameter is NULL, the timer object will cease to queue new callbacks (but callbacks already queued will still occur). Note that if this parameter is zero, the timer will expire immediately.




### -param msPeriod [in]

The timer period, in milliseconds. If this parameter is zero, the timer is signaled once. If this parameter is greater than zero, the timer is periodic. A periodic timer automatically reactivates each time the period elapses, until the timer is canceled.


### -param msWindowLength [in, optional]

The maximum amount of time the system can delay before calling the timer callback. If this parameter is set, the system can batch calls to conserve power. 


## -returns



This function does not return a value.




## -remarks



Setting the timer cancels the previous timer, if any.

In some cases, callback functions might run after an application closes the threadpool timer. To prevent this behavior, an application should call <b>SetThreadpoolTimer</b> with the <i>pftDueTime</i> parameter set to NULL and the <i>msPeriod</i> and <i>msWindowLength</i> parameters set to 0. For more information, see <a href="https://msdn.microsoft.com/c1270c5d-a1f5-4481-a343-c1ff3301a56e">CloseThreadpoolTimer</a>.

If the due time specified by <i>pftDueTime</i> is relative, the time that the system spends in sleep or hibernation does not count toward the expiration of the timer. The timer is signaled when the cumulative amount of elapsed time the system spends in the waking state equals the timer's relative due time or period. If the  due time specified by <i>pftDueTime</i> is absolute, the time that the system spends in sleep or hibernation does count toward the expiration of the timer. If the timer expires while the system is sleeping, the timer is signaled immediately when the system wakes.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c1270c5d-a1f5-4481-a343-c1ff3301a56e">CloseThreadpoolTimer</a>



<a href="https://msdn.microsoft.com/1fa98b79-e646-4e48-9979-1817d2c1b713">CreateThreadpoolTimer</a>



<a href="https://msdn.microsoft.com/f9dee0aa-6310-4218-b207-72a24c5019e2">IsThreadpoolTimerSet</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/511488b8-9e92-47b9-8b3c-7ece9d9f996c">WaitForThreadpoolTimerCallbacks</a>
 

 

