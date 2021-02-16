---
UID: NF:cscobj.IOfflineFilesItem.IsMarkedForDeletion
title: IOfflineFilesItem::IsMarkedForDeletion (cscobj.h)
description: Determines whether an item has been deleted from the Offline Files cache.
helpviewer_keywords: ["IOfflineFilesItem interface [Offline Files]","IsMarkedForDeletion method","IOfflineFilesItem.IsMarkedForDeletion","IOfflineFilesItem::IsMarkedForDeletion","IsMarkedForDeletion","IsMarkedForDeletion method [Offline Files]","IsMarkedForDeletion method [Offline Files]","IOfflineFilesItem interface","cscobj/IOfflineFilesItem::IsMarkedForDeletion","of.iofflinefilesitem_ismarkedfordeletion"]
old-location: of\iofflinefilesitem_ismarkedfordeletion.htm
tech.root: of
ms.assetid: 03c0fec4-d320-4c46-a07c-3ebbec61cc54
ms.date: 12/05/2018
ms.keywords: IOfflineFilesItem interface [Offline Files],IsMarkedForDeletion method, IOfflineFilesItem.IsMarkedForDeletion, IOfflineFilesItem::IsMarkedForDeletion, IsMarkedForDeletion, IsMarkedForDeletion method [Offline Files], IsMarkedForDeletion method [Offline Files],IOfflineFilesItem interface, cscobj/IOfflineFilesItem::IsMarkedForDeletion, of.iofflinefilesitem_ismarkedfordeletion
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
 - IOfflineFilesItem::IsMarkedForDeletion
 - cscobj/IOfflineFilesItem::IsMarkedForDeletion
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
 - IOfflineFilesItem.IsMarkedForDeletion
---

# IOfflineFilesItem::IsMarkedForDeletion


## -description

Determines whether an item has been deleted from the Offline Files cache.

## -parameters

### -param pbMarkedForDeletion [out]

Receives <b>TRUE</b> if the item has been deleted, or <b>FALSE</b> otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

Due to internal (in-memory) caching of data structures in the remote file system and the CSC driver, deletion of an item might not remove the item from the cache immediately.  An item is first marked for deletion then, after all handles have closed, the item is removed from the cache.  This behavior is most apparent for share items.

Clients should normally treat such items as if they do not exist in the cache.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a>