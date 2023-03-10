---
UID: NF:cscobj.IOfflineFilesItem.GetParentItem
title: IOfflineFilesItem::GetParentItem (cscobj.h)
description: Retrieves the IOfflineFilesItem interface for the parent of the item.
helpviewer_keywords: ["GetParentItem","GetParentItem method [Offline Files]","GetParentItem method [Offline Files]","IOfflineFilesItem interface","IOfflineFilesItem interface [Offline Files]","GetParentItem method","IOfflineFilesItem.GetParentItem","IOfflineFilesItem::GetParentItem","cscobj/IOfflineFilesItem::GetParentItem","of.iofflinefilesitem_getparentitem"]
old-location: of\iofflinefilesitem_getparentitem.htm
tech.root: of
ms.assetid: 4fa89807-cd0c-4868-bd65-a8a0a42dff7d
ms.date: 12/05/2018
ms.keywords: GetParentItem, GetParentItem method [Offline Files], GetParentItem method [Offline Files],IOfflineFilesItem interface, IOfflineFilesItem interface [Offline Files],GetParentItem method, IOfflineFilesItem.GetParentItem, IOfflineFilesItem::GetParentItem, cscobj/IOfflineFilesItem::GetParentItem, of.iofflinefilesitem_getparentitem
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
 - IOfflineFilesItem::GetParentItem
 - cscobj/IOfflineFilesItem::GetParentItem
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
 - IOfflineFilesItem.GetParentItem
---

# IOfflineFilesItem::GetParentItem


## -description

Retrieves the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a> interface for the parent of the item. This method can be called repeatedly to retrieve items at the top of the cache namespace.

## -parameters

### -param ppItem [out]

Receives the address of the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a> interface of the parent item.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

If the item is a server item, this function returns <code>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</code>.  Server items are at the top of the Offline Files cache namespace and do not have a parent item.  The parent of a server item is the cache itself.  This is represented by the fact that an instance of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a> is also a container of server items.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a>