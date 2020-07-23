---
UID: NF:synchapi.ReleaseSRWLockExclusive
title: ReleaseSRWLockExclusive function (synchapi.h)
description: Releases a slim reader/writer (SRW) lock that was acquired in exclusive mode.
helpviewer_keywords: ["ReleaseSRWLockExclusive","ReleaseSRWLockExclusive function","base.releasesrwlockexclusive","synchapi/ReleaseSRWLockExclusive","winbase/ReleaseSRWLockExclusive"]
old-location: base\releasesrwlockexclusive.htm
tech.root: backup
ms.assetid: 77f9b8ee-f922-4bd1-b715-ccb1ca891dcc
ms.date: 06/29/2020
ms.keywords: ReleaseSRWLockExclusive, ReleaseSRWLockExclusive function, base.releasesrwlockexclusive, synchapi/ReleaseSRWLockExclusive, winbase/ReleaseSRWLockExclusive
f1_keywords:
- synchapi/ReleaseSRWLockExclusive
dev_langs:
- c++
req.header: synchapi.h
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
- API-MS-Win-Core-Synch-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-Synch-l1-2-0.dll
- API-MS-Win-Core-Synch-l1-2-1.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
- vertdll.dll
api_name:
- ReleaseSRWLockExclusive
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReleaseSRWLockExclusive function


## -description


Releases a slim reader/writer (SRW) lock that was acquired in exclusive mode.


## -parameters




### -param SRWLock [in, out]

A pointer to the SRW lock.


## -remarks

The SRW lock must be released by the same thread that acquired it. You can use [Application Verifier](https://docs.microsoft.com/windows-hardware/drivers/devtest/application-verifier) to help verify that your program uses SRW locks correctly (enable Locks checker from Basic group).


## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-acquiresrwlockexclusive">AcquireSRWLockExclusive</a>

<a href="https://docs.microsoft.com/windows/desktop/Sync/slim-reader-writer--srw--locks">Slim Reader/Writer (SRW) Locks</a>

<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

