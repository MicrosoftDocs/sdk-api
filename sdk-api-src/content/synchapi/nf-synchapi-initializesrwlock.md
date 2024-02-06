---
UID: NF:synchapi.InitializeSRWLock
title: InitializeSRWLock function (synchapi.h)
description: Initialize a slim reader/writer (SRW) lock.
helpviewer_keywords: ["InitializeSRWLock","InitializeSRWLock function","base.initializesrwlock","synchapi/InitializeSRWLock","winbase/InitializeSRWLock"]
old-location: base\initializesrwlock.htm
tech.root: base
ms.assetid: a94443e1-009c-49ba-a51c-6daa63b07cda
ms.date: 02/05/2024
ms.keywords: InitializeSRWLock, InitializeSRWLock function, base.initializesrwlock, synchapi/InitializeSRWLock, winbase/InitializeSRWLock
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
 - InitializeSRWLock
 - synchapi/InitializeSRWLock
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
 - InitializeSRWLock
---

# InitializeSRWLock function

## -description

Initialize a slim reader/writer (SRW) lock.

## -parameters

### -param SRWLock [out]

A pointer to the SRW lock.

## -remarks

An SRW lock must be initialized before it is used. The InitializeSRWLock function is used to initialize a SRW lock dynamically. To initialize the structure statically, assign the constant **SRWLOCK_INIT** to the structure variable.

An SRW lock cannot be moved or copied while in use. The process must not modify the object, and must instead treat it as logically opaque. Only use the SRW functions to manage SRW locks.

An unlocked SRW lock with no waiting threads is in its initial state and can be copied, moved, and forgotten without being explicitly destroyed.

## -see-also

[Slim Reader/Writer (SRW) Locks](/windows/win32/Sync/slim-reader-writer--srw--locks)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
