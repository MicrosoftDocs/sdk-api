---
UID: NF:cscobj.IOfflineFilesItem.Refresh
title: IOfflineFilesItem::Refresh
author: windows-sdk-content
description: Refreshes any data cached in the object by rereading from the Offline Files cache.
old-location: of\iofflinefilesitem_refresh.htm
tech.root: OfflineFiles
ms.assetid: 7b54d6fa-18b6-4ffb-98ce-4cbc44ed5b77
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesItem interface [Offline Files],Refresh method, IOfflineFilesItem.Refresh, IOfflineFilesItem::Refresh, Refresh, Refresh method [Offline Files], Refresh method [Offline Files],IOfflineFilesItem interface, cscobj/IOfflineFilesItem::Refresh, of.iofflinefilesitem_refresh
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
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - IOfflineFilesItem::Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cscobj.h
: 
- IOfflineFilesItem.Refresh
: 
---

# IOfflineFilesItem::Refresh


## -description


Refreshes any data cached in the object by rereading from the Offline Files cache. 


## -parameters




### -param dwQueryFlags [in] [in]

TBD


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.

<code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code> if the file does not exist in the cache.  This would happen if a file has been deleted from the cache after the file object was first created.




## -remarks



When a file object is first created, its internal data is initialized with information from the Offline Files cache.  It is possible that while an object is held in memory, its true state in the cache can change at any time.  Calling <b>Refresh</b> updates the object with the latest information from the Offline Files cache.




## -see-also




<a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a>
 

 

