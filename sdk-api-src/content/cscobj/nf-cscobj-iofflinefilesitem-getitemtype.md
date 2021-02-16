---
UID: NF:cscobj.IOfflineFilesItem.GetItemType
title: IOfflineFilesItem::GetItemType (cscobj.h)
description: Returns a type code identifying the type of the item:\_server, share, directory, or file.
helpviewer_keywords: ["GetItemType","GetItemType method [Offline Files]","GetItemType method [Offline Files]","IOfflineFilesItem interface","IOfflineFilesItem interface [Offline Files]","GetItemType method","IOfflineFilesItem.GetItemType","IOfflineFilesItem::GetItemType","cscobj/IOfflineFilesItem::GetItemType","of.iofflinefilesitem_getitemtype"]
old-location: of\iofflinefilesitem_getitemtype.htm
tech.root: of
ms.assetid: 87fbf63a-d103-4c80-b6a7-60784c7350bc
ms.date: 12/05/2018
ms.keywords: GetItemType, GetItemType method [Offline Files], GetItemType method [Offline Files],IOfflineFilesItem interface, IOfflineFilesItem interface [Offline Files],GetItemType method, IOfflineFilesItem.GetItemType, IOfflineFilesItem::GetItemType, cscobj/IOfflineFilesItem::GetItemType, of.iofflinefilesitem_getitemtype
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
 - IOfflineFilesItem::GetItemType
 - cscobj/IOfflineFilesItem::GetItemType
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
 - IOfflineFilesItem.GetItemType
---

# IOfflineFilesItem::GetItemType


## -description

Returns a type code identifying the type of the item: server, share, directory, or file.

## -parameters

### -param pItemType [out]

Receives an <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_type">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

Another way to determine an item's type is to query the item for one of the following type-specific interfaces:

<a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesdirectoryitem">IOfflineFilesDirectoryItem</a>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesfileitem">IOfflineFilesFileItem</a>
<a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesserveritem">IOfflineFilesServerItem</a>
<a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesshareitem">IOfflineFilesShareItem</a>
If the call to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> succeeds, the item is of the requested type.  An item can be of only one of the above types.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a>