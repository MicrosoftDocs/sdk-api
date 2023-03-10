---
UID: NF:cscobj.IOfflineFilesEvents.SyncFileResult
title: IOfflineFilesEvents::SyncFileResult (cscobj.h)
description: Reports the result of synchronizing a particular file.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","SyncFileResult method","IOfflineFilesEvents.SyncFileResult","IOfflineFilesEvents::SyncFileResult","SyncFileResult","SyncFileResult method [Offline Files]","SyncFileResult method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::SyncFileResult","of.iofflinefilesevents_syncfileresult"]
old-location: of\iofflinefilesevents_syncfileresult.htm
tech.root: of
ms.assetid: 3770e966-7481-449e-9b57-44a7329d26db
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],SyncFileResult method, IOfflineFilesEvents.SyncFileResult, IOfflineFilesEvents::SyncFileResult, SyncFileResult, SyncFileResult method [Offline Files], SyncFileResult method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::SyncFileResult, of.iofflinefilesevents_syncfileresult
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
 - IOfflineFilesEvents::SyncFileResult
 - cscobj/IOfflineFilesEvents::SyncFileResult
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
 - IOfflineFilesEvents.SyncFileResult
---

# IOfflineFilesEvents::SyncFileResult


## -description

Reports the result of synchronizing a particular file.

## -parameters

### -param rSyncId [in]

Unique identifier for the synchronization operation that generated this event.  Provided by the caller of the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-synchronize">IOfflineFilesCache::Synchronize</a>, <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a>, or <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-unpin">IOfflineFilesCache::Unpin</a> method.  This is GUID_NULL if no ID was provided.

### -param pszFile [in]

Fully qualified UNC path of the processed file.

### -param hrResult [in]

Result of the sync operation on this file.  The parameter will contain S_OK if the operation completed successfully or a value otherwise.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>