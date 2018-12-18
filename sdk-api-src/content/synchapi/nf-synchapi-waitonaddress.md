---
UID: NF:synchapi.WaitOnAddress
title: WaitOnAddress function
author: windows-sdk-content
description: Waits for the value at the specified address to change.
old-location: base\waitonaddress.htm
tech.root: sync
ms.assetid: d40de436-f71e-47f6-a8c3-549c2699eb4c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WaitOnAddress, WaitOnAddress function, base.waitonaddress, synchapi/WaitOnAddress
ms.topic: function
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Synchronization.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - MinKernelBase.dll
api_name:
 - WaitOnAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WaitOnAddress function


## -description


Waits for the value at the specified address to change.


## -parameters




### -param Address [in]

The address on which to wait. If the value at <i>Address</i> differs from the value at <i>CompareAddress</i>, the function returns immediately. If the values are the same, the function does not return until another thread in the same process signals that the value at Address has changed by calling <a href="https://msdn.microsoft.com/4ca8f7b9-e78e-4324-9e72-84267746fe53">WakeByAddressSingle</a> or <a href="https://msdn.microsoft.com/2d538cea-06cb-4973-8677-27ebcde0aa6f">WakeByAddressAll</a> or the timeout elapses, whichever comes first.


### -param CompareAddress [in]

A pointer to the location of the previously observed value at <i>Address</i>. The function returns when the value at <i>Address</i> differs from the value at <i>CompareAddress</i>.


### -param AddressSize [in]

The size of the value, in bytes. This parameter can be 1, 2, 4, or 8. 


### -param dwMilliseconds [in, optional]

The number of milliseconds to wait before the operation times out. If this parameter is <b>INFINITE</b>, the thread waits indefinitely.


## -returns



TRUE if the wait succeeded. If the operation fails, the function returns FALSE. If the wait fails, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to obtain extended error information. In particular, if the operation times out, <b>GetLastError</b>  returns <b>ERROR_TIMEOUT</b>.




## -remarks



Windows Store apps developers may need to obtain synchronization.lib by installing the <a href="http://go.microsoft.com/fwlink/p/?LinkID=258383">Windows Software Development Kit (SDK) for Windows 8</a>.

The <b>WaitOnAddress</b> function can be used by a thread to wait for a particular value to change from some undesired value to any other value. <b>WaitOnAddress</b> is more efficient than using the <a href="https://msdn.microsoft.com/934d37ea-402c-4118-bd7e-87b5fce80fca">Sleep</a> function inside a <b>while</b> loop because <b>WaitOnAddress</b> does not interfere with the thread scheduler. <b>WaitOnAddress</b> is also simpler to use than an event object because it is not necessary to create and initialize an event and then make sure it is synchronized correctly with the value. <b>WaitOnAddress</b> is not affected by low-memory conditions, other than potentially waking the thread early as noted below.

Any thread within the same  process that changes the value at the address on which threads are waiting should call <a href="https://msdn.microsoft.com/4ca8f7b9-e78e-4324-9e72-84267746fe53">WakeByAddressSingle</a> to wake a single waiting thread or  <a href="https://msdn.microsoft.com/2d538cea-06cb-4973-8677-27ebcde0aa6f">WakeByAddressAll</a> to wake all waiting threads. If <b>WakeByAddressSingle</b> is called, other waiting threads continue to wait.

<div class="alert"><b>Note</b>  <b>WaitOnAddress</b> is guaranteed to return when the address is signaled, but it is also allowed to return for other reasons. For this reason, after <b>WaitOnAddress</b> returns the caller should compare the new value with the original undesired value to confirm that the value has actually changed. For example, the following circumstances can result in waking the thread early:<ul>
<li>Low memory conditions</li>
<li>A previous wake on the same address was abandoned</li>
<li>Executing code on a checked build of the operating system</li>
</ul>
</div>
<div> </div>

#### Examples

The following example shows how to use <b>WaitOnAddress</b>.

<pre class="syntax" xml:space="preserve"><code>ULONG g_TargetValue; // global, accessible to all threads
ULONG CapturedValue;
ULONG UndesiredValue;

UndesiredValue = 0;
CapturedValue = g_TargetValue;
while (CapturedValue == UndesiredValue) {
      WaitOnAddress(&amp;g_TargetValue, &amp;UndesiredValue, sizeof(ULONG), INFINITE);
      CapturedValue = g_TargetValue;
}
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/2d538cea-06cb-4973-8677-27ebcde0aa6f">WakeByAddressAll</a>



<a href="https://msdn.microsoft.com/4ca8f7b9-e78e-4324-9e72-84267746fe53">WakeByAddressSingle</a>
 

 

