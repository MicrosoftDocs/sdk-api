---
UID: NF:cscobj.IOfflineFilesEvents2.BackgroundSyncBegin
title: IOfflineFilesEvents2::BackgroundSyncBegin
author: windows-sdk-content
description: Reports that the Offline Files service is beginning to perform a background synchronization pass.
old-location: of\iofflinefilesevents2_backgroundsyncbegin.htm
old-project: offlinefiles
ms.assetid: 84b71228-904a-4042-8d13-422ae77f7ba5
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: BackgroundSyncBegin, BackgroundSyncBegin method [Offline Files], BackgroundSyncBegin method [Offline Files],IOfflineFilesEvents2 interface, IOfflineFilesEvents2 interface [Offline Files],BackgroundSyncBegin method, IOfflineFilesEvents2.BackgroundSyncBegin, IOfflineFilesEvents2::BackgroundSyncBegin, cscobj/IOfflineFilesEvents2::BackgroundSyncBegin, of.iofflinefilesevents2_backgroundsyncbegin
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesEvents2.BackgroundSyncBegin
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents2::BackgroundSyncBegin


## -description


Reports that the Offline Files service is beginning to perform a background synchronization pass.


## -parameters




### -param dwSyncControlFlags [in]

One or more OFFLINEFILES_SYNC_CONTROL_FLAG_XXXXXX flags describing the purpose of the sync operation.  These may be used to determine if the sync is a one-way or two-way sync. These flags are described in the <i>dwSyncControl</i> parameter of the <a href="https://msdn.microsoft.com/4a9dd105-ea68-40ce-b1cb-6126ca932095">IOfflineFilesCache::Synchronize</a> method.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/746f7220-8c87-4218-bd97-ec9b862e549c">IOfflineFilesEvents2</a>
 

 

