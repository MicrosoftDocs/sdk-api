---
UID: NF:synchapi.ReleaseSRWLockShared
title: ReleaseSRWLockShared function
author: windows-sdk-content
description: Releases a slim reader/writer (SRW) lock that was acquired in shared mode.
old-location: base\releasesrwlockshared.htm
tech.root: Sync
ms.assetid: afefd9f2-7fd4-4cba-9a6f-1f9da614dcec
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ReleaseSRWLockShared, ReleaseSRWLockShared function, base.releasesrwlockshared, synchapi/ReleaseSRWLockShared, winbase/ReleaseSRWLockShared
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
 - ReleaseSRWLockShared
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReleaseSRWLockShared function


## -description


Releases a slim reader/writer (SRW) lock that was acquired in shared mode.


## -parameters




### -param SRWLock [in, out]

A pointer to the SRW lock.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/86e6d915-c25d-4aee-9ec6-acb970da7069">AcquireSRWLockShared</a>



<a href="https://msdn.microsoft.com/2d439b21-291f-4ff0-910a-c1c27e800019">Slim Reader/Writer (SRW) Locks</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

