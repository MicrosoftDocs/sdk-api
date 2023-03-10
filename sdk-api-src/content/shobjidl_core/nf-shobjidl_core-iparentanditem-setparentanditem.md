---
UID: NF:shobjidl_core.IParentAndItem.SetParentAndItem
title: IParentAndItem::SetParentAndItem (shobjidl_core.h)
description: Sets the parent of an item and the parent's child ID.
helpviewer_keywords: ["IParentAndItem interface [Windows Shell]","SetParentAndItem method","IParentAndItem.SetParentAndItem","IParentAndItem::SetParentAndItem","SetParentAndItem","SetParentAndItem method [Windows Shell]","SetParentAndItem method [Windows Shell]","IParentAndItem interface","_shell_IParentAndItem_SetParentAndItem","shell.IParentAndItem_SetParentAndItem","shobjidl_core/IParentAndItem::SetParentAndItem"]
old-location: shell\IParentAndItem_SetParentAndItem.htm
tech.root: shell
ms.assetid: 398bb0c1-39f1-4a51-9382-421639ab7b8e
ms.date: 12/05/2018
ms.keywords: IParentAndItem interface [Windows Shell],SetParentAndItem method, IParentAndItem.SetParentAndItem, IParentAndItem::SetParentAndItem, SetParentAndItem, SetParentAndItem method [Windows Shell], SetParentAndItem method [Windows Shell],IParentAndItem interface, _shell_IParentAndItem_SetParentAndItem, shell.IParentAndItem_SetParentAndItem, shobjidl_core/IParentAndItem::SetParentAndItem
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
 - IParentAndItem::SetParentAndItem
 - shobjidl_core/IParentAndItem::SetParentAndItem
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
 - IParentAndItem.SetParentAndItem
---

# IParentAndItem::SetParentAndItem


## -description

Sets the parent of an item and the parent's child ID.

## -parameters

### -param pidlParent [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer of the parent.

### -param psf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> that is the parent.

### -param pidlChild [in]

Type: <b>PCUITEMID_CHILD</b>

A PIDL that is a child relative to <i>psf</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 While <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem">IParentAndItem</a> is typically implemented on IShellItems, it is not specific to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.