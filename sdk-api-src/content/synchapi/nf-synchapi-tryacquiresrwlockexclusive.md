---
UID: NF:synchapi.TryAcquireSRWLockExclusive
title: TryAcquireSRWLockExclusive function (synchapi.h)
description: Attempts to acquire a slim reader/writer (SRW) lock in exclusive mode. If the call is successful, the calling thread takes ownership of the lock.
helpviewer_keywords: ["TryAcquireSRWLockExclusive","TryAcquireSRWLockExclusive function","base.tryacquiresrwlockexclusive","synchapi/TryAcquireSRWLockExclusive","winbase/TryAcquireSRWLockExclusive"]
old-location: base\tryacquiresrwlockexclusive.htm
tech.root: backup
ms.assetid: 0de41cb0-5b37-4ac7-9ba2-e9e3d69e34af
ms.date: 12/05/2018
ms.keywords: TryAcquireSRWLockExclusive, TryAcquireSRWLockExclusive function, base.tryacquiresrwlockexclusive, synchapi/TryAcquireSRWLockExclusive, winbase/TryAcquireSRWLockExclusive
f1_keywords:
- synchapi/TryAcquireSRWLockExclusive
dev_langs:
- c++
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
api_name:
- TryAcquireSRWLockExclusive
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TryAcquireSRWLockExclusive function


## -description


Attempts to acquire a slim reader/writer (SRW) lock in exclusive mode. If the call is successful, the calling thread takes ownership of the lock. 


## -parameters




### -param SRWLock [in, out]

A pointer to the SRW lock.


## -returns



If the lock is successfully acquired, the return value is nonzero.

if the current thread could not acquire the lock, the return value is zero.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-acquiresrwlockexclusive">AcquireSRWLockExclusive</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/slim-reader-writer--srw--locks">Slim Reader/Writer (SRW) Locks</a>



<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-tryacquiresrwlockshared">TryAcquireSRWLockShared</a>
 

 

