---
UID: NF:cscobj.IOfflineFilesFileItem.IsSparse
title: IOfflineFilesFileItem::IsSparse
author: windows-sdk-content
description: Determines whether an item in the Offline Files cache is sparsely cached.
old-location: of\iofflinefilesfileitem_issparse.htm
old-project: offlinefiles
ms.assetid: 6f731b25-f4f0-4635-af00-dbd1ba4e5f11
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: IOfflineFilesFileItem interface [Offline Files],IsSparse method, IOfflineFilesFileItem.IsSparse, IOfflineFilesFileItem::IsSparse, IsSparse, IsSparse method [Offline Files], IsSparse method [Offline Files],IOfflineFilesFileItem interface, cscobj/IOfflineFilesFileItem::IsSparse, of.iofflinefilesfileitem_issparse
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
 - IOfflineFilesFileItem.IsSparse
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesFileItem::IsSparse


## -description


Determines whether an item in the Offline Files cache is sparsely cached.


## -parameters




### -param pbIsSparse [out]

Receives <b>TRUE</b> if the item is sparsely cached, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



A sparsely cached item is an item that has an entry in the Offline Files cache but is not completely cached; not all of its data blocks have been read into the cache.  Such items must first be filled before they are available for offline use.  The Offline Files service automatically fills sparse files on a frequent schedule.

To fill sparse files manually, use the <a href="https://msdn.microsoft.com/4a9dd105-ea68-40ce-b1cb-6126ca932095">IOfflineFilesCache::Synchronize</a> method, setting the OFFLINEFILES_SYNC_CONTROL_FLAG_FILLSPARSE control flag in the <i>dwSyncControl</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/53b9af4b-7526-4b54-bae2-61c97aa67ebf">IOfflineFilesFileItem</a>
 

 

