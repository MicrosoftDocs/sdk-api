---
UID: NF:cscobj.IOfflineFilesEvents.ItemNotAvailableOffline
title: IOfflineFilesEvents::ItemNotAvailableOffline (cscobj.h)
description: Reports that an item in the Offline Files cache is no longer available for offline use should the remote copy become unavailable.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","ItemNotAvailableOffline method","IOfflineFilesEvents.ItemNotAvailableOffline","IOfflineFilesEvents::ItemNotAvailableOffline","ItemNotAvailableOffline","ItemNotAvailableOffline method [Offline Files]","ItemNotAvailableOffline method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::ItemNotAvailableOffline","of.iofflinefilesevents_itemnotavailableoffline"]
old-location: of\iofflinefilesevents_itemnotavailableoffline.htm
tech.root: of
ms.assetid: 868938fd-9da2-45fd-a00e-5dda85b4fd61
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemNotAvailableOffline method, IOfflineFilesEvents.ItemNotAvailableOffline, IOfflineFilesEvents::ItemNotAvailableOffline, ItemNotAvailableOffline, ItemNotAvailableOffline method [Offline Files], ItemNotAvailableOffline method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemNotAvailableOffline, of.iofflinefilesevents_itemnotavailableoffline
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
 - IOfflineFilesEvents::ItemNotAvailableOffline
 - cscobj/IOfflineFilesEvents::ItemNotAvailableOffline
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
 - IOfflineFilesEvents.ItemNotAvailableOffline
---

# IOfflineFilesEvents::ItemNotAvailableOffline


## -description

Reports that an item in the Offline Files cache is no longer available for offline use should the remote copy become unavailable.

## -parameters

### -param pszPath [in]

The item's UNC path string.

### -param ItemType [in]

An <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_type">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.

## -returns

The return value is ignored.

## -remarks

Receipt of this event does not mean the file has been removed from the cache.  The event <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents-itemdeletedfromcache">ItemDeletedFromCache</a> is sent when an item has been removed.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>