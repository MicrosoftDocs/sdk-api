---
UID: NF:shobjidl_core.IRelatedItem.GetItem
title: IRelatedItem::GetItem (shobjidl_core.h)
description: Gets the IShellItem that is related to this item.
helpviewer_keywords: ["GetItem","GetItem method [Windows Shell]","GetItem method [Windows Shell]","IRelatedItem interface","IRelatedItem interface [Windows Shell]","GetItem method","IRelatedItem.GetItem","IRelatedItem::GetItem","_shell_IRelatedItem_GetItem","shell.IRelatedItem_GetItem","shobjidl_core/IRelatedItem::GetItem"]
old-location: shell\IRelatedItem_GetItem.htm
tech.root: shell
ms.assetid: 4aaf0016-1a0d-49ef-a001-bc4a7fe90758
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [Windows Shell], GetItem method [Windows Shell],IRelatedItem interface, IRelatedItem interface [Windows Shell],GetItem method, IRelatedItem.GetItem, IRelatedItem::GetItem, _shell_IRelatedItem_GetItem, shell.IRelatedItem_GetItem, shobjidl_core/IRelatedItem::GetItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRelatedItem::GetItem
 - shobjidl_core/IRelatedItem::GetItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IRelatedItem.GetItem
---

# IRelatedItem::GetItem


## -description

Gets the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that is related to this item.

## -parameters

### -param ppsi

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

When this method returns, contains the address of a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interface for the item that is related to this item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.