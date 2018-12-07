---
UID: NF:cscobj.IOfflineFilesEvents.SyncFileResult
title: IOfflineFilesEvents::SyncFileResult
author: windows-sdk-content
description: Reports the result of synchronizing a particular file.
old-location: of\iofflinefilesevents_syncfileresult.htm
tech.root: offlinefiles
ms.assetid: 3770e966-7481-449e-9b57-44a7329d26db
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],SyncFileResult method, IOfflineFilesEvents.SyncFileResult, IOfflineFilesEvents::SyncFileResult, SyncFileResult, SyncFileResult method [Offline Files], SyncFileResult method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::SyncFileResult, of.iofflinefilesevents_syncfileresult
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
 - IOfflineFilesEvents.SyncFileResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents::SyncFileResult


## -description


Reports the result of synchronizing a particular file.


## -parameters




### -param rSyncId [in]

Unique identifier for the synchronization operation that generated this event.  Provided by the caller of the <a href="https://msdn.microsoft.com/en-us/library/Bb530502(v=VS.85).aspx">IOfflineFilesCache::Synchronize</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb530498(v=VS.85).aspx">IOfflineFilesCache::Pin</a>, or <a href="https://msdn.microsoft.com/en-us/library/Bb530503(v=VS.85).aspx">IOfflineFilesCache::Unpin</a> method.  This is GUID_NULL if no ID was provided.


### -param pszFile [in]

Fully qualified UNC path of the processed file.


### -param hrResult [in]

Result of the sync operation on this file.  The parameter will contain S_OK if the operation completed successfully or an value otherwise.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>
 

 

