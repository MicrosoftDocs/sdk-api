---
UID: NF:synchapi.WaitOnAddress
title: WaitOnAddress function (synchapi.h)
description: Waits for the value at the specified address to change.
helpviewer_keywords: ["WaitOnAddress","WaitOnAddress function","base.waitonaddress","synchapi/WaitOnAddress"]
old-location: base\waitonaddress.htm
tech.root: base
ms.assetid: d40de436-f71e-47f6-a8c3-549c2699eb4c
ms.date: 02/05/2024
ms.keywords: WaitOnAddress, WaitOnAddress function, base.waitonaddress, synchapi/WaitOnAddress
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
req.dll: API-MS-Win-Core-Synch-l1-2-0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WaitOnAddress
 - synchapi/WaitOnAddress
dev_langs:
 - c++
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
 - vertdll.dll
api_name:
 - WaitOnAddress
---

# WaitOnAddress function

## -description

Waits for the value at the specified address to change.

## -parameters

### -param Address [in]

The address on which to wait. If the value at *Address* differs from the value at *CompareAddress*, the function returns immediately. If the values are the same, the function does not return until another thread in the same process signals that the value at Address has changed by calling [WakeByAddressSingle](nf-synchapi-wakebyaddresssingle.md) or [WakeByAddressAll](nf-synchapi-wakebyaddressall.md) or the timeout elapses, whichever comes first.

### -param CompareAddress [in]

A pointer to the location of the previously observed value at *Address*. The function returns when the value at *Address* differs from the value at *CompareAddress*.

### -param AddressSize [in]

The size of the value, in bytes. This parameter can be `1`, `2`, `4`, or `8`.

### -param dwMilliseconds [in, optional]

The number of milliseconds to wait before the operation times out. If this parameter is **INFINITE**, the thread waits indefinitely.

## -returns

`TRUE` if the wait succeeded. If the operation fails, the function returns `FALSE`. If the wait fails, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) to obtain extended error information. In particular, if the operation times out, **GetLastError** returns **ERROR_TIMEOUT**.

## -remarks

Microsoft Store app developers may need to obtain `synchronization.lib` by installing the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-sdk/).

The **WaitOnAddress** function can be used by a thread to wait for a particular value to change from some undesired value to any other value. **WaitOnAddress** is more efficient than using the [Sleep](nf-synchapi-sleep.md) function inside a `while` loop because **WaitOnAddress** does not interfere with the thread scheduler. **WaitOnAddress** is also simpler to use than an event object because it is not necessary to create and initialize an event and then make sure it is synchronized correctly with the value. **WaitOnAddress** is not affected by low-memory conditions, other than potentially waking the thread early as noted below.

Any thread within the same  process that changes the value at the address on which threads are waiting should call [WakeByAddressSingle](nf-synchapi-wakebyaddresssingle.md) to wake a single waiting thread or  [WakeByAddressAll](nf-synchapi-wakebyaddressall.md) to wake all waiting threads. If **WakeByAddressSingle** is called, other waiting threads continue to wait.

<div class="alert"><b>Note:</b> <b>WaitOnAddress</b> is guaranteed to return when the address is signaled, but it is also allowed to return for other reasons. For this reason, after <b>WaitOnAddress</b> returns the caller should compare the new value with the original undesired value to confirm that the value has actually changed. For example, the following circumstances can result in waking the thread early:<ul>
<li>Low memory conditions</li>
<li>A previous wake on the same address was abandoned</li>
<li>Executing code on a checked build of the operating system</li>
</ul>
</div>
<div> </div>

#### Examples

The following example shows how to use **WaitOnAddress**.

``` cpp
ULONG g_TargetValue; // global, accessible to all threads
ULONG CapturedValue;
ULONG UndesiredValue;

UndesiredValue = 0;
CapturedValue = g_TargetValue;
while (CapturedValue == UndesiredValue) {
      WaitOnAddress(&g_TargetValue, &UndesiredValue, sizeof(ULONG), INFINITE);
      CapturedValue = g_TargetValue;
}
```

## -see-also

[WakeByAddressAll](nf-synchapi-wakebyaddressall.md)

[WakeByAddressSingle](nf-synchapi-wakebyaddresssingle.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
