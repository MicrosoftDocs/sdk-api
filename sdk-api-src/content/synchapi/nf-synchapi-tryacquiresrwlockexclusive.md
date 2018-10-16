---
UID: NF:synchapi.TryAcquireSRWLockExclusive
title: TryAcquireSRWLockExclusive function
author: windows-sdk-content
description: Attempts to acquire a slim reader/writer (SRW) lock in exclusive mode. If the call is successful, the calling thread takes ownership of the lock.
old-location: base\tryacquiresrwlockexclusive.htm
tech.root: sync
ms.assetid: 0de41cb0-5b37-4ac7-9ba2-e9e3d69e34af
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: TryAcquireSRWLockExclusive, TryAcquireSRWLockExclusive function, base.tryacquiresrwlockexclusive, synchapi/TryAcquireSRWLockExclusive, winbase/TryAcquireSRWLockExclusive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/02e987a2-4c2f-4ccb-8816-c04320b568c1">AcquireSRWLockExclusive</a>



<a href="https://msdn.microsoft.com/2d439b21-291f-4ff0-910a-c1c27e800019">Slim Reader/Writer (SRW) Locks</a>



<a href="https://msdn.microsoft.com/e7b0c273-c1d4-4a1c-a824-f519fb52ad8f">TryAcquireSRWLockShared</a>
 

 

