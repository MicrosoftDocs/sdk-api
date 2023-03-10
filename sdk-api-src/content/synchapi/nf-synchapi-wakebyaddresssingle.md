---
UID: NF:synchapi.WakeByAddressSingle
title: WakeByAddressSingle function (synchapi.h)
description: Wakes one thread that is waiting for the value of an address to change.
helpviewer_keywords: ["WakeByAddressSingle","WakeByAddressSingle function","base.wakebyaddresssingle","synchapi/WakeByAddressSingle"]
old-location: base\wakebyaddresssingle.htm
tech.root: base
ms.assetid: 4ca8f7b9-e78e-4324-9e72-84267746fe53
ms.date: 12/05/2018
ms.keywords: WakeByAddressSingle, WakeByAddressSingle function, base.wakebyaddresssingle, synchapi/WakeByAddressSingle
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
 - WakeByAddressSingle
 - synchapi/WakeByAddressSingle
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
api_name:
 - WakeByAddressSingle
---

# WakeByAddressSingle function


## -description

Wakes one thread that is waiting for the value of an address to change.

## -parameters

### -param Address [in]

The address to signal. If another thread has previously called 
      <a href="/windows/desktop/api/synchapi/nf-synchapi-waitonaddress">WaitOnAddress</a> for this address, the system wakes the 
      waiting thread. If multiple threads are waiting for this address, the system wakes the first thread to 
      wait.

## -remarks

Windows Store apps developers may need to obtain synchronization.lib by installing the <a href="https://developer.microsoft.com/en-us/windows/downloads/windows-8-sdk">Windows Software Development Kit (SDK) for Windows 8</a>.

Only a thread within the same process can be woken.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-waitonaddress">WaitOnAddress</a>
