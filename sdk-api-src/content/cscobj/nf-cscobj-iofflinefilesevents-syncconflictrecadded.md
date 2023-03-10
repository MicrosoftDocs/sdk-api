---
UID: NF:cscobj.IOfflineFilesEvents.SyncConflictRecAdded
title: IOfflineFilesEvents::SyncConflictRecAdded (cscobj.h)
description: Reports that a sync conflict has been detected and recorded in the sync conflict log.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","SyncConflictRecAdded method","IOfflineFilesEvents.SyncConflictRecAdded","IOfflineFilesEvents::SyncConflictRecAdded","SyncConflictRecAdded","SyncConflictRecAdded method [Offline Files]","SyncConflictRecAdded method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::SyncConflictRecAdded","of.iofflinefilesevents_syncconflictrecadded"]
old-location: of\iofflinefilesevents_syncconflictrecadded.htm
tech.root: of
ms.assetid: 693306de-d968-4857-8221-965b2f271aae
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],SyncConflictRecAdded method, IOfflineFilesEvents.SyncConflictRecAdded, IOfflineFilesEvents::SyncConflictRecAdded, SyncConflictRecAdded, SyncConflictRecAdded method [Offline Files], SyncConflictRecAdded method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::SyncConflictRecAdded, of.iofflinefilesevents_syncconflictrecadded
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
 - IOfflineFilesEvents::SyncConflictRecAdded
 - cscobj/IOfflineFilesEvents::SyncConflictRecAdded
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
 - IOfflineFilesEvents.SyncConflictRecAdded
---

# IOfflineFilesEvents::SyncConflictRecAdded


## -description

Reports that a sync conflict has been detected and recorded in the sync conflict log.

## -parameters

### -param pszConflictPath [in]

The UNC path of the item in conflict.

### -param pftConflictDateTime [in]

Pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the date and time when the conflict was detected.  The value is in UTC.

### -param ConflictSyncState [in]

Describes the state of the local and remote items in conflict.  One of the <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_sync_state">OFFLINEFILES_SYNC_STATE</a> sync state values, such as

OFFLINEFILES_SYNC_STATE_FileChangedOnClient_ChangedOnServer

.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>