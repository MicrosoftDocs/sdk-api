---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

