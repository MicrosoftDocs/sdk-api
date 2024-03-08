---
UID: NF:synchapi.AcquireSRWLockExclusive
title: AcquireSRWLockExclusive function (synchapi.h)
description: Acquires a slim reader/writer (SRW) lock in exclusive mode.
helpviewer_keywords: ["AcquireSRWLockExclusive","AcquireSRWLockExclusive function","base.acquiresrwlockexclusive","synchapi/AcquireSRWLockExclusive","winbase/AcquireSRWLockExclusive"]
old-location: base\acquiresrwlockexclusive.htm
tech.root: base
ms.assetid: 02e987a2-4c2f-4ccb-8816-c04320b568c1
ms.date: 02/05/2024
ms.keywords: AcquireSRWLockExclusive, AcquireSRWLockExclusive function, base.acquiresrwlockexclusive, synchapi/AcquireSRWLockExclusive, winbase/AcquireSRWLockExclusive
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
 - AcquireSRWLockExclusive
 - synchapi/AcquireSRWLockExclusive
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
 - vertdll.dll
api_name:
 - AcquireSRWLockExclusive
---

# AcquireSRWLockExclusive function

## -description

Acquires a slim reader/writer (SRW) lock in exclusive mode.

## -parameters

### -param SRWLock [in, out]

A pointer to the SRW lock.

## -see-also

[ReleaseSRWLockExclusive](nf-synchapi-releasesrwlockexclusive.md)

[Slim Reader/Writer (SRW) Locks](/windows/win32/Sync/slim-reader-writer--srw--locks)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
