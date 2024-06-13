---
UID: NF:synchapi.AcquireSRWLockShared
title: AcquireSRWLockShared function (synchapi.h)
description: Acquires a slim reader/writer (SRW) lock in shared mode.
helpviewer_keywords: ["AcquireSRWLockShared","AcquireSRWLockShared function","base.acquiresrwlockshared","synchapi/AcquireSRWLockShared","winbase/AcquireSRWLockShared"]
old-location: base\acquiresrwlockshared.htm
tech.root: base
ms.assetid: 86e6d915-c25d-4aee-9ec6-acb970da7069
ms.date: 3/08/2024
ms.keywords: AcquireSRWLockShared, AcquireSRWLockShared function, base.acquiresrwlockshared, synchapi/AcquireSRWLockShared, winbase/AcquireSRWLockShared
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
 - AcquireSRWLockShared
 - synchapi/AcquireSRWLockShared
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
 - AcquireSRWLockShared
---

# AcquireSRWLockShared function

## -description

Acquires a slim reader/writer (SRW) lock in shared mode.

## -parameters

### -param SRWLock [in, out]

A pointer to the SRW lock.

## -Remarks

Successful acquisition of an SRW lock in shared mode typically permits other threads to acquire the same lock in shared mode, but doesn't guarantee that such acquisitions always succeed. An SRW lock may limit its simultaneous shared mode acquisitions for performance reasons.

## -see-also

[ReleaseSRWLockShared](nf-synchapi-releasesrwlockshared.md)

[Slim Reader/Writer (SRW) Locks](/windows/win32/Sync/slim-reader-writer--srw--locks)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
