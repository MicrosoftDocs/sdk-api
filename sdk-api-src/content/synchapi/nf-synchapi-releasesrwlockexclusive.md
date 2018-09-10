---
UID: NF:synchapi.ReleaseSRWLockExclusive
title: ReleaseSRWLockExclusive function
author: windows-sdk-content
description: Releases a slim reader/writer (SRW) lock that was acquired in exclusive mode.
old-location: base\releasesrwlockexclusive.htm
tech.root: Sync
ms.assetid: 77f9b8ee-f922-4bd1-b715-ccb1ca891dcc
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ReleaseSRWLockExclusive, ReleaseSRWLockExclusive function, base.releasesrwlockexclusive, synchapi/ReleaseSRWLockExclusive, winbase/ReleaseSRWLockExclusive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - ReleaseSRWLockExclusive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReleaseSRWLockExclusive function


## -description


Releases a slim reader/writer (SRW) lock that was acquired in exclusive mode.


## -parameters




### -param SRWLock [in, out]

A pointer to the SRW lock.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/02e987a2-4c2f-4ccb-8816-c04320b568c1">AcquireSRWLockExclusive</a>



<a href="https://msdn.microsoft.com/2d439b21-291f-4ff0-910a-c1c27e800019">Slim Reader/Writer (SRW) Locks</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

