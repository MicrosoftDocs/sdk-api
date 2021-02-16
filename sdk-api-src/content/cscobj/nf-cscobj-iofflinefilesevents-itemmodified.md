---
UID: NF:cscobj.IOfflineFilesEvents.ItemModified
title: IOfflineFilesEvents::ItemModified (cscobj.h)
description: Reports that an item in the Offline Files cache has been modified.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","ItemModified method","IOfflineFilesEvents.ItemModified","IOfflineFilesEvents::ItemModified","ItemModified","ItemModified method [Offline Files]","ItemModified method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::ItemModified","of.iofflinefilesevents_itemmodified"]
old-location: of\iofflinefilesevents_itemmodified.htm
tech.root: of
ms.assetid: e689b111-d6d1-436e-b468-570e575a5170
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemModified method, IOfflineFilesEvents.ItemModified, IOfflineFilesEvents::ItemModified, ItemModified, ItemModified method [Offline Files], ItemModified method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemModified, of.iofflinefilesevents_itemmodified
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
 - IOfflineFilesEvents::ItemModified
 - cscobj/IOfflineFilesEvents::ItemModified
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
 - IOfflineFilesEvents.ItemModified
---

# IOfflineFilesEvents::ItemModified


## -description

Reports that an item in the Offline Files cache has been modified.

## -parameters

### -param pszPath [in]

The item's UNC path string.

### -param ItemType [in]

An <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_type">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.

### -param bModifiedData [in]

<b>TRUE</b> if the item's data was modified, <b>FALSE</b> otherwise.

### -param bModifiedAttributes [in]

<b>TRUE</b> if one or more of the item's attributes were modified, <b>FALSE</b> otherwise.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>