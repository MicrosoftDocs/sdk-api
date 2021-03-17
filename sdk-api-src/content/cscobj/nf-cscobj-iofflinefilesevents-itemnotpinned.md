---
UID: NF:cscobj.IOfflineFilesEvents.ItemNotPinned
title: IOfflineFilesEvents::ItemNotPinned (cscobj.h)
description: Reports that an item in the Offline Files cache is no longer pinned.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","ItemNotPinned method","IOfflineFilesEvents.ItemNotPinned","IOfflineFilesEvents::ItemNotPinned","ItemNotPinned","ItemNotPinned method [Offline Files]","ItemNotPinned method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::ItemNotPinned","of.iofflinefilesevents_itemnotpinned"]
old-location: of\iofflinefilesevents_itemnotpinned.htm
tech.root: of
ms.assetid: cefd7408-9e98-48a4-ad43-0bdef9da1c95
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemNotPinned method, IOfflineFilesEvents.ItemNotPinned, IOfflineFilesEvents::ItemNotPinned, ItemNotPinned, ItemNotPinned method [Offline Files], ItemNotPinned method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemNotPinned, of.iofflinefilesevents_itemnotpinned
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
 - IOfflineFilesEvents::ItemNotPinned
 - cscobj/IOfflineFilesEvents::ItemNotPinned
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
 - IOfflineFilesEvents.ItemNotPinned
---

# IOfflineFilesEvents::ItemNotPinned


## -description

Reports that an item in the Offline Files cache is no longer pinned.  The item may still be available offline but it is now considered automatically cached.

## -parameters

### -param pszPath [in]

The item's UNC path string.

### -param ItemType [in]

An <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_type">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>