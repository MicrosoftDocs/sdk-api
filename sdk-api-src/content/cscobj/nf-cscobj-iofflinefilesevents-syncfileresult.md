---
UID: NF:cscobj.IOfflineFilesEvents.SyncFileResult
title: IOfflineFilesEvents::SyncFileResult method
author: windows-driver-content
description: Reports the result of synchronizing a particular file.
old-location: of\iofflinefilesevents_syncfileresult.htm
old-project: OfflineFiles
ms.assetid: 3770e966-7481-449e-9b57-44a7329d26db
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOfflineFilesEvents, IOfflineFilesEvents interface [Offline Files], SyncFileResult method, IOfflineFilesEvents::SyncFileResult, SyncFileResult method [Offline Files], SyncFileResult method [Offline Files], IOfflineFilesEvents interface, SyncFileResult,IOfflineFilesEvents.SyncFileResult, cscobj/IOfflineFilesEvents::SyncFileResult, of.iofflinefilesevents_syncfileresult
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
-	IOfflineFilesEvents.SyncFileResult
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents::SyncFileResult method


## -description


Reports the result of synchronizing a particular file.


## -parameters




### -param rSyncId [in]

Unique identifier for the synchronization operation that generated this event.  Provided by the caller of the <a href="https://msdn.microsoft.com/4a9dd105-ea68-40ce-b1cb-6126ca932095">IOfflineFilesCache::Synchronize</a>, <a href="https://msdn.microsoft.com/6005d755-5e1b-4eba-95a2-b6c9c00b1a64">IOfflineFilesCache::Pin</a>, or <a href="https://msdn.microsoft.com/32d81a75-8845-4bd5-a0ff-e056a06ac11c">IOfflineFilesCache::Unpin</a> method.  This is GUID_NULL if no ID was provided.


### -param pszFile [in]

Fully qualified UNC path of the processed file.


### -param hrResult [in]

Result of the sync operation on this file.  The parameter will contain S_OK if the operation completed successfully or an value otherwise.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

