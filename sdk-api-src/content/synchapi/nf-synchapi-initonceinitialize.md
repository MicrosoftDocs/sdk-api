---
UID: NF:synchapi.InitOnceInitialize
title: InitOnceInitialize function (synchapi.h)
description: Initializes a one-time initialization structure.
helpviewer_keywords: ["InitOnceInitialize","InitOnceInitialize function","base.initonceinitialize","synchapi/InitOnceInitialize","winbase/InitOnceInitialize"]
old-location: base\initonceinitialize.htm
tech.root: base
ms.assetid: f2943ac5-0e43-4f07-8941-952383e2fa08
ms.date: 12/05/2018
ms.keywords: InitOnceInitialize, InitOnceInitialize function, base.initonceinitialize, synchapi/InitOnceInitialize, winbase/InitOnceInitialize
req.header: synchapi.h
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
 - InitOnceInitialize
 - synchapi/InitOnceInitialize
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
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - InitOnceInitialize
---

# InitOnceInitialize function


## -description

Initializes a one-time initialization structure.

## -parameters

### -param InitOnce [out]

A pointer to the one-time initialization structure.

## -remarks

The <b>InitOnceInitialize</b> function is used to initialize a one-time initialization structure dynamically. To initialize the structure statically, assign the constant <b>INIT_ONCE_STATIC_INIT</b> to the structure variable.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

A one-time initialization object cannot be moved or copied. The process must not modify the initialization object, and must instead treat it as logically opaque. Only use the one-time initialization functions to manage one-time initialization objects.


#### Examples

The following example calls <b>InitOnceInitialize</b> to initialize the one-time initialization structure named <code>InitOnce</code>. Alternatively, the structure can be declared as a global variable as shown in <a href="/windows/desktop/Sync/using-one-time-initialization">Using One-Time Initialization</a>.


```cpp

//Requires Windows Vista, Windows Server 2008 or later
#define _WIN32_WINNT 0x0600

#include <windows.h>

BOOL StartInitialization()
{
    INIT_ONCE InitOnce;

    InitOnceInitialize(&InitOnce);

    //...
    return TRUE;
}

```

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-initonceexecuteonce">InitOnceExecuteOnce</a>



<a href="/windows/desktop/Sync/one-time-initialization">One-Time Initialization</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>