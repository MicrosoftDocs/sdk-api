---
UID: NF:cscobj.IOfflineFilesEvents.SyncBegin
title: IOfflineFilesEvents::SyncBegin (cscobj.h)
description: Reports that the Offline Files cache has begun a synchronization operation.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","SyncBegin method","IOfflineFilesEvents.SyncBegin","IOfflineFilesEvents::SyncBegin","SyncBegin","SyncBegin method [Offline Files]","SyncBegin method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::SyncBegin","of.iofflinefilesevents_syncbegin"]
old-location: of\iofflinefilesevents_syncbegin.htm
tech.root: of
ms.assetid: ba09be0a-52bc-4715-9756-383954277a31
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],SyncBegin method, IOfflineFilesEvents.SyncBegin, IOfflineFilesEvents::SyncBegin, SyncBegin, SyncBegin method [Offline Files], SyncBegin method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::SyncBegin, of.iofflinefilesevents_syncbegin
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesEvents::SyncBegin
 - cscobj/IOfflineFilesEvents::SyncBegin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesEvents.SyncBegin
---

# IOfflineFilesEvents::SyncBegin


## -description

Reports that the Offline Files cache has begun a synchronization operation.

## -parameters

### -param rSyncId [in]

Unique identifier for the synchronization operation that generated this event.  Provided by the caller of the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-synchronize">IOfflineFilesCache::Synchronize</a>, <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a>, or <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-unpin">IOfflineFilesCache::Unpin</a> method.  This is GUID_NULL if no ID was provided.

## -returns

The return value is ignored.

## -remarks

The synchronization engine is also used to encrypt the Offline Files cache.  Therefore, encryption and unencryption operations will also cause this event to be generated.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>