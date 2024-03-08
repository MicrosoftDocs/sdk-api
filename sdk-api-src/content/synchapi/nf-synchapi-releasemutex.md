---
UID: NF:synchapi.ReleaseMutex
title: ReleaseMutex function (synchapi.h)
description: Releases ownership of the specified mutex object.
helpviewer_keywords: ["ReleaseMutex","ReleaseMutex function","_win32_releasemutex","base.releasemutex","synchapi/ReleaseMutex","winbase/ReleaseMutex"]
old-location: base\releasemutex.htm
tech.root: base
ms.assetid: c3e4daa8-92de-455c-847c-ea59225b3aa2
ms.date: 12/05/2018
ms.keywords: ReleaseMutex, ReleaseMutex function, _win32_releasemutex, base.releasemutex, synchapi/ReleaseMutex, winbase/ReleaseMutex
req.header: synchapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - ReleaseMutex
 - synchapi/ReleaseMutex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - ReleaseMutex
---

# ReleaseMutex function


## -description

Releases ownership of the specified mutex object.

## -parameters

### -param hMutex [in]

A handle to the mutex object. The 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a> or 

<a href="/windows/win32/api/synchapi/nf-synchapi-openmutexw">OpenMutex</a> function returns this handle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>ReleaseMutex</b> function fails if the calling thread does not own the mutex object.

A thread obtains ownership of a mutex either by creating it with the <i>bInitialOwner</i> parameter set to <b>TRUE</b> or by specifying its handle in a call to one of the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>. When the thread no longer needs to own the mutex object, it calls the 
<b>ReleaseMutex</b> function so that another thread can acquire ownership.

A thread  can specify a  mutex that it already owns in a call to one of the wait functions without blocking its execution. This prevents a thread from deadlocking itself while waiting for a mutex that it already owns. However, to release its ownership, the thread must call 
<b>ReleaseMutex</b> one time for each time that it obtained ownership (either through <a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a> or a wait function).


#### Examples

For an example that uses 
<b>ReleaseMutex</b>, see 
<a href="/windows/desktop/Sync/using-mutex-objects">Using Mutex Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a>



<a href="/windows/desktop/Sync/mutex-objects">Mutex Objects</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>