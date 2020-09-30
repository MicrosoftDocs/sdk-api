---
UID: NF:synchapi.TryAcquireSRWLockShared
title: TryAcquireSRWLockShared function (synchapi.h)
description: Attempts to acquire a slim reader/writer (SRW) lock in shared mode. If the call is successful, the calling thread takes ownership of the lock.
helpviewer_keywords: ["TryAcquireSRWLockShared","TryAcquireSRWLockShared function","base.tryacquiresrwlockshared","synchapi/TryAcquireSRWLockShared","winbase/TryAcquireSRWLockShared"]
old-location: base\tryacquiresrwlockshared.htm
tech.root: backup
ms.assetid: e7b0c273-c1d4-4a1c-a824-f519fb52ad8f
ms.date: 12/05/2018
ms.keywords: TryAcquireSRWLockShared, TryAcquireSRWLockShared function, base.tryacquiresrwlockshared, synchapi/TryAcquireSRWLockShared, winbase/TryAcquireSRWLockShared
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - TryAcquireSRWLockShared
 - synchapi/TryAcquireSRWLockShared
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - ntdll.dll
api_name:
 - TryAcquireSRWLockShared
 - RtlTryAcquireSRWLockShared
---

# TryAcquireSRWLockShared function


## -description

Attempts to acquire a slim reader/writer (SRW) lock in shared mode. If the call is successful, the calling thread takes ownership of the lock.

## -parameters

### -param SRWLock [in, out]

A pointer to the SRW lock.

## -returns

If the lock is successfully acquired, the return value is nonzero.

if the current thread could not acquire the lock, the return value is zero.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-acquiresrwlockshared">AcquireSRWLockShared</a>



<a href="/windows/desktop/Sync/slim-reader-writer--srw--locks">Slim Reader/Writer (SRW) Locks</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive">TryAcquireSRWLockExclusive</a>