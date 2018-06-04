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

# ITsSbResourcePluginStore::AcquireTargetLock


## -description


Locks a target.


## -parameters




### -param targetName [in]

The name of the target to lock.


### -param dwTimeout [in]

The timeout for the operation, in milliseconds.


### -param ppContext [out]

Returns a pointer to the context of the lock. To release the lock, supply this pointer to the <a href="https://msdn.microsoft.com/37c22f94-c00d-471b-bd6c-067b3229f99b">ReleaseTargetLock</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After the lock is acquired, the calling thread is assumed to have exclusive access to the target object and therefore no other thread (within the same machine) can update it. Therefore the calling thread must call the <a href="https://msdn.microsoft.com/37c22f94-c00d-471b-bd6c-067b3229f99b">ReleaseTargetLock</a> method as soon as it has made the necessary updates to the target object.

<div class="alert"><b>Important</b>  this lock does not completely prevent target objects from being modified externally if more than one Connection Broker exists in the deployment. The calling thread must be prepared to handle a failure gracefully and retry the target update.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>
 

 

