---
UID: NF:synchapi.WakeByAddressAll
title: WakeByAddressAll function (synchapi.h)
description: Wakes all threads that are waiting for the value of an address to change.
helpviewer_keywords: ["WakeByAddressAll","WakeByAddressAll function","base.wakebyaddressall","synchapi/WakeByAddressAll"]
old-location: base\wakebyaddressall.htm
tech.root: base
ms.assetid: 2d538cea-06cb-4973-8677-27ebcde0aa6f
ms.date: 02/05/2024
ms.keywords: WakeByAddressAll, WakeByAddressAll function, base.wakebyaddressall, synchapi/WakeByAddressAll
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
 - WakeByAddressAll
 - synchapi/WakeByAddressAll
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
 - WakeByAddressAll
---

# WakeByAddressAll function

## -description

Wakes all threads that are waiting for the value of an address to change.

## -parameters

### -param Address [in]

The address to signal. If any threads have previously called [WaitOnAddress](nf-synchapi-waitonaddress.md) for this address, the system wakes all of the waiting threads.

## -remarks

Microsoft Store app developers may need to obtain `synchronization.lib` by installing the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-sdk/).

Only threads within the same process can be woken.

## -see-also

[WaitOnAddress](nf-synchapi-waitonaddress.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
