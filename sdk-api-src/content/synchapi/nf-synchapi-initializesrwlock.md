---
UID: NF:synchapi.InitializeSRWLock
title: InitializeSRWLock function (synchapi.h)

description: Initialize a slim reader/writer (SRW) lock.
old-location: base\initializesrwlock.htm
tech.root: Sync
ms.assetid: a94443e1-009c-49ba-a51c-6daa63b07cda

ms.date: 12/05/2018
ms.keywords: InitializeSRWLock, InitializeSRWLock function, base.initializesrwlock, synchapi/InitializeSRWLock, winbase/InitializeSRWLock
ms.topic: function
f1_keywords: 
 - "synchapi/InitializeSRWLock"
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
api_name:
 - InitializeSRWLock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InitializeSRWLock function


## -description


Initialize a slim reader/writer (SRW) lock.


## -parameters




### -param SRWLock [out]

A pointer to the SRW lock.


## -returns



This function does not return a value.




## -remarks



An SRW lock must be initialized before it is used. The InitializeSRWLock function is used to initialize a SRW lock dynamically. To initialize the structure statically, assign the constant <b>SRWLOCK_INIT</b> to the structure variable.

An SRW lock cannot be moved or copied. The process must not modify the object, and must instead treat it as logically opaque. Only use the SRW functions to manage SRW locks. 

SRW locks do not need to be explicitly destroyed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/slim-reader-writer--srw--locks">Slim Reader/Writer (SRW) Locks</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

