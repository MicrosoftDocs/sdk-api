---
UID: NF:cscobj.IOfflineFilesEvents.ItemRenamed
title: IOfflineFilesEvents::ItemRenamed (cscobj.h)
description: Reports that the path for an item in the Offline Files cache has been renamed.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","ItemRenamed method","IOfflineFilesEvents.ItemRenamed","IOfflineFilesEvents::ItemRenamed","ItemRenamed","ItemRenamed method [Offline Files]","ItemRenamed method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::ItemRenamed","of.iofflinefilesevents_itemrenamed"]
old-location: of\iofflinefilesevents_itemrenamed.htm
tech.root: of
ms.assetid: f1a678dd-9a02-41da-90d4-930c0d366a36
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemRenamed method, IOfflineFilesEvents.ItemRenamed, IOfflineFilesEvents::ItemRenamed, ItemRenamed, ItemRenamed method [Offline Files], ItemRenamed method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemRenamed, of.iofflinefilesevents_itemrenamed
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
 - IOfflineFilesEvents::ItemRenamed
 - cscobj/IOfflineFilesEvents::ItemRenamed
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
 - IOfflineFilesEvents.ItemRenamed
---

# IOfflineFilesEvents::ItemRenamed


## -description

Reports that the path for an item in the Offline Files cache has been renamed.

## -parameters

### -param pszOldPath [in]

Original UNC path string for the item.

### -param pszNewPath [in]

New UNC path string for the item.

### -param ItemType [in]

An <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_type">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.

## -returns

The return value is ignored.

## -remarks

This event is sent whenever a server, share, directory or file is renamed in the cache.  Note that this is a rename resulting from a file system rename operation, not from <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-renameitem">IOfflineFilesCache::RenameItem</a> or <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache2-renameitemex">IOfflineFilesCache2::RenameItemEx</a>.  (The rename in response to <b>RenameItem</b> or <b>RenameItemEx</b> is performed on system startup by the Offline Files driver before the Offline Files service is operational.)

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>