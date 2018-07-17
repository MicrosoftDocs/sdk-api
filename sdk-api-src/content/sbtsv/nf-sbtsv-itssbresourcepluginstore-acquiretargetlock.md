---
UID: NF:sbtsv.ITsSbResourcePluginStore.AcquireTargetLock
title: ITsSbResourcePluginStore::AcquireTargetLock
author: windows-sdk-content
description: Locks a target.
old-location: termserv\itssbresourcepluginstore_acquiretargetlock.htm
old-project: termserv
ms.assetid: ee6f22cf-c111-4a11-ab84-b52904a148b6
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: AcquireTargetLock, AcquireTargetLock method [Remote Desktop Services], AcquireTargetLock method [Remote Desktop Services],ITsSbResourcePluginStore interface, ITsSbResourcePluginStore interface [Remote Desktop Services],AcquireTargetLock method, ITsSbResourcePluginStore.AcquireTargetLock, ITsSbResourcePluginStore::AcquireTargetLock, sbtsv/ITsSbResourcePluginStore::AcquireTargetLock, termserv.itssbresourcepluginstore_acquiretargetlock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.AcquireTargetLock
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

