---
UID: NF:sbtsv.ITsSbResourcePluginStore.ReleaseTargetLock
title: ITsSbResourcePluginStore::ReleaseTargetLock (sbtsv.h)
description: Releases a lock on a target.
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","ReleaseTargetLock method","ITsSbResourcePluginStore.ReleaseTargetLock","ITsSbResourcePluginStore::ReleaseTargetLock","ReleaseTargetLock","ReleaseTargetLock method [Remote Desktop Services]","ReleaseTargetLock method [Remote Desktop Services]","ITsSbResourcePluginStore interface","sbtsv/ITsSbResourcePluginStore::ReleaseTargetLock","termserv.itssbresourcepluginstore_releasetargetlock"]
old-location: termserv\itssbresourcepluginstore_releasetargetlock.htm
tech.root: TermServ
ms.assetid: 37c22f94-c00d-471b-bd6c-067b3229f99b
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],ReleaseTargetLock method, ITsSbResourcePluginStore.ReleaseTargetLock, ITsSbResourcePluginStore::ReleaseTargetLock, ReleaseTargetLock, ReleaseTargetLock method [Remote Desktop Services], ReleaseTargetLock method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::ReleaseTargetLock, termserv.itssbresourcepluginstore_releasetargetlock
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
 - ITsSbResourcePluginStore::ReleaseTargetLock
 - sbtsv/ITsSbResourcePluginStore::ReleaseTargetLock
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
 - ITsSbResourcePluginStore.ReleaseTargetLock
---

# ITsSbResourcePluginStore::ReleaseTargetLock


## -description

Releases a lock on a target.

## -parameters

### -param pContext [in]

A pointer to the context returned by the <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock">AcquireTargetLock</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>