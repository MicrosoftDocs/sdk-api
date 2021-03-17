---
UID: NF:cscobj.IOfflineFilesEvents.SyncEnd
title: IOfflineFilesEvents::SyncEnd (cscobj.h)
description: Reports that the Offline Files cache has ended a synchronize operation.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","SyncEnd method","IOfflineFilesEvents.SyncEnd","IOfflineFilesEvents::SyncEnd","SyncEnd","SyncEnd method [Offline Files]","SyncEnd method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::SyncEnd","of.iofflinefilesevents_syncend"]
old-location: of\iofflinefilesevents_syncend.htm
tech.root: of
ms.assetid: 2b4b32b9-7268-4f79-8eac-640a6c62b0c1
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],SyncEnd method, IOfflineFilesEvents.SyncEnd, IOfflineFilesEvents::SyncEnd, SyncEnd, SyncEnd method [Offline Files], SyncEnd method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::SyncEnd, of.iofflinefilesevents_syncend
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
 - IOfflineFilesEvents::SyncEnd
 - cscobj/IOfflineFilesEvents::SyncEnd
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
 - IOfflineFilesEvents.SyncEnd
---

# IOfflineFilesEvents::SyncEnd


## -description

Reports that the Offline Files cache has ended a synchronize operation.

## -parameters

### -param rSyncId [in]

Unique identifier for the synchronization operation that generated this event.  Provided by the caller of the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-synchronize">IOfflineFilesCache::Synchronize</a>, <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a>, or <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-unpin">IOfflineFilesCache::Unpin</a> method.  This is GUID_NULL if no ID was provided.

### -param hrResult [in]

Result value indicating the reason for the end of the sync operation.  This parameter will be S_OK if the operation completed successfully, HRESULT_FROM_WIN32(ERROR_CANCELLED) if the operation was aborted and an error value if some other failure caused the operation to complete prematurely.

## -returns

The return value is ignored.

## -remarks

The sync engine is also used to encrypted the Offline Files cache.  Therefore, an encryption or unencryption operation will cause this event to be generated.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>