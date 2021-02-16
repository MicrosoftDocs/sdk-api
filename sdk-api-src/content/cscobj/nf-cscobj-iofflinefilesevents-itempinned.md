---
UID: NF:cscobj.IOfflineFilesEvents.ItemPinned
title: IOfflineFilesEvents::ItemPinned (cscobj.h)
description: Reports that an item in the Offline Files cache is now pinned and guaranteed to be available offline should the remote copy become unavailable.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","ItemPinned method","IOfflineFilesEvents.ItemPinned","IOfflineFilesEvents::ItemPinned","ItemPinned","ItemPinned method [Offline Files]","ItemPinned method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::ItemPinned","of.iofflinefilesevents_itempinned"]
old-location: of\iofflinefilesevents_itempinned.htm
tech.root: of
ms.assetid: cf298e4e-97c8-4f6f-b6f5-0bd0d9435599
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemPinned method, IOfflineFilesEvents.ItemPinned, IOfflineFilesEvents::ItemPinned, ItemPinned, ItemPinned method [Offline Files], ItemPinned method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemPinned, of.iofflinefilesevents_itempinned
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
 - IOfflineFilesEvents::ItemPinned
 - cscobj/IOfflineFilesEvents::ItemPinned
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
 - IOfflineFilesEvents.ItemPinned
---

# IOfflineFilesEvents::ItemPinned


## -description

Reports that an item in the Offline Files cache is now pinned and guaranteed to be available offline should the remote copy become unavailable.

## -parameters

### -param pszPath [in]

The item's UNC path string.

### -param ItemType [in]

An <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_type">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>