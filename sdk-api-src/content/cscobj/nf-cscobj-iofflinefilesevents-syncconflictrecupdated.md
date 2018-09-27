---
UID: NF:cscobj.IOfflineFilesEvents.SyncConflictRecUpdated
title: IOfflineFilesEvents::SyncConflictRecUpdated
author: windows-sdk-content
description: Reports that a sync conflict has been detected and that a record of the conflict was already present in the sync conflict log.
old-location: of\iofflinefilesevents_syncconflictrecupdated.htm
tech.root: OfflineFiles
ms.assetid: adf13e95-bcb0-4f84-bbb9-9648f90f3be8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],SyncConflictRecUpdated method, IOfflineFilesEvents.SyncConflictRecUpdated, IOfflineFilesEvents::SyncConflictRecUpdated, SyncConflictRecUpdated, SyncConflictRecUpdated method [Offline Files], SyncConflictRecUpdated method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::SyncConflictRecUpdated, of.iofflinefilesevents_syncconflictrecupdated
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesEvents.SyncConflictRecUpdated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents::SyncConflictRecUpdated


## -description


Reports that a sync conflict has been detected and that a record of the conflict was already present in the sync conflict log. The log's record has been updated with the latest information.


## -parameters




### -param pszConflictPath [in]

The UNC path of the item in conflict.


### -param pftConflictDateTime [in]

Pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the date and time when the conflict was detected.  The value is in UTC.


### -param ConflictSyncState [in]

Describes the state of the local and remote items in conflict.  One of the <a href="https://msdn.microsoft.com/en-us/library/Bb530655(v=VS.85).aspx">OFFLINEFILES_SYNC_STATE</a> sync state values, such as

OFFLINEFILES_SYNC_STATE_FileChangedOnClient_ChangedOnServer

.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>
 

 

