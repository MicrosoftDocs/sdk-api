---
UID: NF:shobjidl.IInsertItem.InsertItem
title: IInsertItem::InsertItem (shobjidl.h)
description: Adds an ITEMIDLIST structure to a list of such structures.
helpviewer_keywords: ["IInsertItem interface [Windows Shell]","InsertItem method","IInsertItem.InsertItem","IInsertItem::InsertItem","InsertItem","InsertItem method [Windows Shell]","InsertItem method [Windows Shell]","IInsertItem interface","shell.IInsertitem_InsertItem","shell_IInsertitem_InsertItem","shobjidl/IInsertItem::InsertItem"]
old-location: shell\IInsertitem_InsertItem.htm
tech.root: shell
ms.assetid: 45a25357-9bb1-4298-9ffb-20081e3072a5
ms.date: 12/05/2018
ms.keywords: IInsertItem interface [Windows Shell],InsertItem method, IInsertItem.InsertItem, IInsertItem::InsertItem, InsertItem, InsertItem method [Windows Shell], InsertItem method [Windows Shell],IInsertItem interface, shell.IInsertitem_InsertItem, shell_IInsertitem_InsertItem, shobjidl/IInsertItem::InsertItem
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IInsertItem::InsertItem
 - shobjidl/IInsertItem::InsertItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IInsertItem.InsertItem
---

# IInsertItem::InsertItem


## -description

Adds an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure to a list of such structures.

## -parameters

### -param pidl [in]

Type: <b>LPCITEMIDLIST</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that corresponds to an item in a Shell folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.