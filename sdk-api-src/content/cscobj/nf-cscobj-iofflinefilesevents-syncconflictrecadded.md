---
UID: NF:cscobj.IOfflineFilesEvents.SyncConflictRecAdded
title: IOfflineFilesEvents::SyncConflictRecAdded
author: windows-driver-content
description: Reports that a sync conflict has been detected and recorded in the sync conflict log.
old-location: of\iofflinefilesevents_syncconflictrecadded.htm
old-project: OfflineFiles
ms.assetid: 693306de-d968-4857-8221-965b2f271aae
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],SyncConflictRecAdded method, IOfflineFilesEvents.SyncConflictRecAdded, IOfflineFilesEvents::SyncConflictRecAdded, SyncConflictRecAdded, SyncConflictRecAdded method [Offline Files], SyncConflictRecAdded method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::SyncConflictRecAdded, of.iofflinefilesevents_syncconflictrecadded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CscSvc.dll
-	CscObj.dll
api_name:
-	IOfflineFilesEvents.SyncConflictRecAdded
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents::SyncConflictRecAdded


## -description


Reports that a sync conflict has been detected and recorded in the sync conflict log.


## -parameters




### -param pszConflictPath [in]

The UNC path of the item in conflict.


### -param pftConflictDateTime [in]

Pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the date and time when the conflict was detected.  The value is in UTC.


### -param ConflictSyncState [in]

Describes the state of the local and remote items in conflict.  One of the <a href="https://msdn.microsoft.com/05d1e03e-2db4-4f1e-8813-98c8cf6d03b6">OFFLINEFILES_SYNC_STATE</a> sync state values, such as

OFFLINEFILES_SYNC_STATE_FileChangedOnClient_ChangedOnServer

.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

