---
UID: NF:cscobj.IOfflineFilesItem.Refresh
title: IOfflineFilesItem::Refresh (cscobj.h)
description: Refreshes any data cached in the object by rereading from the Offline Files cache.
helpviewer_keywords: ["IOfflineFilesItem interface [Offline Files]","Refresh method","IOfflineFilesItem.Refresh","IOfflineFilesItem::Refresh","Refresh","Refresh method [Offline Files]","Refresh method [Offline Files]","IOfflineFilesItem interface","cscobj/IOfflineFilesItem::Refresh","of.iofflinefilesitem_refresh"]
old-location: of\iofflinefilesitem_refresh.htm
tech.root: of
ms.assetid: 7b54d6fa-18b6-4ffb-98ce-4cbc44ed5b77
ms.date: 12/05/2018
ms.keywords: IOfflineFilesItem interface [Offline Files],Refresh method, IOfflineFilesItem.Refresh, IOfflineFilesItem::Refresh, Refresh, Refresh method [Offline Files], Refresh method [Offline Files],IOfflineFilesItem interface, cscobj/IOfflineFilesItem::Refresh, of.iofflinefilesitem_refresh
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
 - IOfflineFilesItem::Refresh
 - cscobj/IOfflineFilesItem::Refresh
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - IOfflineFilesItem::Refresh
---

# IOfflineFilesItem::Refresh


## -description

Refreshes any data cached in the object by rereading from the Offline Files cache.

## -parameters

### -param dwQueryFlags [in]

TBD

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

<code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code> if the file does not exist in the cache.  This would happen if a file has been deleted from the cache after the file object was first created.

## -remarks

When a file object is first created, its internal data is initialized with information from the Offline Files cache.  It is possible that while an object is held in memory, its true state in the cache can change at any time.  Calling <b>Refresh</b> updates the object with the latest information from the Offline Files cache.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a>