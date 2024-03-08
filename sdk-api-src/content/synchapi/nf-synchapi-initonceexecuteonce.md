---
UID: NF:synchapi.InitOnceExecuteOnce
title: InitOnceExecuteOnce function (synchapi.h)
description: Executes the specified function successfully one time. No other threads that specify the same one-time initialization structure can execute the specified function while it is being executed by the current thread.
helpviewer_keywords: ["InitOnceExecuteOnce","InitOnceExecuteOnce function","base.initonceexecuteonce","synchapi/InitOnceExecuteOnce","winbase/InitOnceExecuteOnce"]
old-location: base\initonceexecuteonce.htm
tech.root: base
ms.assetid: 04c161ed-d1b0-4995-b246-cb64cb67ae47
ms.date: 12/05/2018
ms.keywords: InitOnceExecuteOnce, InitOnceExecuteOnce function, base.initonceexecuteonce, synchapi/InitOnceExecuteOnce, winbase/InitOnceExecuteOnce
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
 - InitOnceExecuteOnce
 - synchapi/InitOnceExecuteOnce
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
 - InitOnceExecuteOnce
---

# InitOnceExecuteOnce function


## -description

When multiple threads call InitOnceExecuteOnce passing the same one-time initialization block, only one thread will execute the callback function specified by <i>InitFn</i>. The remaining threads will block until the callback function completes. If the callback function returns <b>TRUE</b> to indicate success, InitOnceExecuteOnce will return <b>TRUE</b> back to all callers at once. If, however, the callback returns <b>FALSE</b> to indicate failure, InitOnceExecuteOnce will return <b>FALSE</b> to only the single thread which executed the callback function. At this same time one of the remaining blocked threads will unblock and execute <i>InitFn</i> once again. Thus, in a scenario where <i>InitFn</i> can fail intermittently and retries are desired, all threads should continue calling InitOnceExecuteOnce until <b>TRUE</b> is returned.

## -parameters

### -param InitOnce [in, out]

A pointer to the one-time initialization structure.

### -param InitFn [in]

A pointer to an application-defined <a href="/windows/desktop/api/synchapi/nc-synchapi-pinit_once_fn">InitOnceCallback</a> function.

### -param Parameter [in, optional]

A parameter to be passed to the callback function.

### -param Context [in, out, optional]

A parameter that receives data stored with the one-time initialization structure upon success. The low-order <b>INIT_ONCE_CTX_RESERVED_BITS</b> bits of the data are always zero. If <i>Context</i> points to a data structure, the data structure must be <b>DWORD</b>-aligned. <i>Context</i> must not be a code pointer on Arm32, because Arm32 code pointers always have the least significant bit set, see the <a href="/cpp/build/overview-of-arm-abi-conventions?view=msvc-170#instruction-set">Arm32 ABI</a> for details.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is used for synchronous one-time initialization. For asynchronous one-time initialization, use the <a href="/windows/desktop/api/synchapi/nf-synchapi-initoncebegininitialize">InitOnceBeginInitialize</a> function with the <b>INIT_ONCE_ASYNC</b> flag.

Only one thread at a time can execute the callback function specified by <i>InitFn</i>. Other threads that specify the same one-time initialization structure block until the callback finishes.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example that uses 
this function, see 
<a href="/windows/desktop/Sync/using-one-time-initialization">Using One-Time Initialization</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/synchapi/nc-synchapi-pinit_once_fn">InitOnceCallback</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-initonceinitialize">InitOnceInitialize</a>



<a href="/windows/desktop/Sync/one-time-initialization">One-Time Initialization</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
