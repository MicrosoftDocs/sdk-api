---
UID: NF:sbtsv.ITsSbResourcePluginStore.AcquireTargetLock
title: ITsSbResourcePluginStore::AcquireTargetLock (sbtsv.h)
description: Locks a target.
helpviewer_keywords: ["AcquireTargetLock","AcquireTargetLock method [Remote Desktop Services]","AcquireTargetLock method [Remote Desktop Services]","ITsSbResourcePluginStore interface","ITsSbResourcePluginStore interface [Remote Desktop Services]","AcquireTargetLock method","ITsSbResourcePluginStore.AcquireTargetLock","ITsSbResourcePluginStore::AcquireTargetLock","sbtsv/ITsSbResourcePluginStore::AcquireTargetLock","termserv.itssbresourcepluginstore_acquiretargetlock"]
old-location: termserv\itssbresourcepluginstore_acquiretargetlock.htm
tech.root: TermServ
ms.assetid: ee6f22cf-c111-4a11-ab84-b52904a148b6
ms.date: 12/05/2018
ms.keywords: AcquireTargetLock, AcquireTargetLock method [Remote Desktop Services], AcquireTargetLock method [Remote Desktop Services],ITsSbResourcePluginStore interface, ITsSbResourcePluginStore interface [Remote Desktop Services],AcquireTargetLock method, ITsSbResourcePluginStore.AcquireTargetLock, ITsSbResourcePluginStore::AcquireTargetLock, sbtsv/ITsSbResourcePluginStore::AcquireTargetLock, termserv.itssbresourcepluginstore_acquiretargetlock
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbResourcePluginStore::AcquireTargetLock
 - sbtsv/ITsSbResourcePluginStore::AcquireTargetLock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.AcquireTargetLock
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

Returns a pointer to the context of the lock. To release the lock, supply this pointer to the <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock">ReleaseTargetLock</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After the lock is acquired, the calling thread is assumed to have exclusive access to the target object and therefore no other thread (within the same machine) can update it. Therefore the calling thread must call the <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock">ReleaseTargetLock</a> method as soon as it has made the necessary updates to the target object.

<div class="alert"><b>Important</b>  this lock does not completely prevent target objects from being modified externally if more than one Connection Broker exists in the deployment. The calling thread must be prepared to handle a failure gracefully and retry the target update.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>