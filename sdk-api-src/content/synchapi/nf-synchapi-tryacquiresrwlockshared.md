---
UID: NF:synchapi.TryAcquireSRWLockShared
title: TryAcquireSRWLockShared function
author: windows-sdk-content
description: Attempts to acquire a slim reader/writer (SRW) lock in shared mode. If the call is successful, the calling thread takes ownership of the lock.
old-location: base\tryacquiresrwlockshared.htm
old-project: sync
ms.assetid: e7b0c273-c1d4-4a1c-a824-f519fb52ad8f
ms.author: windowssdkdev
ms.date: 07/06/2018
ms.keywords: TryAcquireSRWLockShared, TryAcquireSRWLockShared function, base.tryacquiresrwlockshared, synchapi/TryAcquireSRWLockShared, winbase/TryAcquireSRWLockShared
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ITEMPROP, *LPITEMPROP
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
 - TryAcquireSRWLockShared
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
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




<a href="https://msdn.microsoft.com/86e6d915-c25d-4aee-9ec6-acb970da7069">AcquireSRWLockShared</a>



<a href="https://msdn.microsoft.com/2d439b21-291f-4ff0-910a-c1c27e800019">Slim Reader/Writer (SRW) Locks</a>



<a href="https://msdn.microsoft.com/0de41cb0-5b37-4ac7-9ba2-e9e3d69e34af">TryAcquireSRWLockExclusive</a>
 

 

