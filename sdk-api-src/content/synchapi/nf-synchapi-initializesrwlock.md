---
UID: NF:synchapi.InitializeSRWLock
title: InitializeSRWLock function
author: windows-sdk-content
description: Initialize a slim reader/writer (SRW) lock.
old-location: base\initializesrwlock.htm
old-project: sync
ms.assetid: a94443e1-009c-49ba-a51c-6daa63b07cda
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InitializeSRWLock, InitializeSRWLock function, base.initializesrwlock, synchapi/InitializeSRWLock, winbase/InitializeSRWLock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.redist: 
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
tech.root: 
req.typenames: ITEMPROP, *LPITEMPROP
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
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




<a href="https://msdn.microsoft.com/2d439b21-291f-4ff0-910a-c1c27e800019">Slim Reader/Writer (SRW) Locks</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

