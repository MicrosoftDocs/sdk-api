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

# _QUERY_SERVICE_LOCK_STATUSW structure


## -description


Contains information about the lock status of a service control manager database. It is used by the 
<a href="https://msdn.microsoft.com/5139d31b-65f1-41ba-852a-91eab1dc366e">QueryServiceLockStatus</a> function.


## -struct-fields




### -field fIsLocked

The lock status of the database. If this member is nonzero, the database is locked. If it is zero, the database is unlocked.


### -field lpLockOwner

The name of the user who acquired the lock.


### -field dwLockDuration

The time since the lock was first acquired, in seconds.


## -see-also




<a href="https://msdn.microsoft.com/5139d31b-65f1-41ba-852a-91eab1dc366e">QueryServiceLockStatus</a>
 

 

