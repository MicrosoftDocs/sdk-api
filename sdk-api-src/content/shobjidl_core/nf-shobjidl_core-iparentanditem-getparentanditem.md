---
UID: NF:shobjidl_core.IParentAndItem.GetParentAndItem
title: IParentAndItem::GetParentAndItem (shobjidl_core.h)
description: Gets the parent of an item and the parent's child ID.
helpviewer_keywords: ["GetParentAndItem","GetParentAndItem method [Windows Shell]","GetParentAndItem method [Windows Shell]","IParentAndItem interface","IParentAndItem interface [Windows Shell]","GetParentAndItem method","IParentAndItem.GetParentAndItem","IParentAndItem::GetParentAndItem","_shell_IParentAndItem_GetParentAndItem","shell.IParentAndItem_GetParentAndItem","shobjidl_core/IParentAndItem::GetParentAndItem"]
old-location: shell\IParentAndItem_GetParentAndItem.htm
tech.root: shell
ms.assetid: 351ad043-949c-46e1-a6cd-bcc15016f42a
ms.date: 12/05/2018
ms.keywords: GetParentAndItem, GetParentAndItem method [Windows Shell], GetParentAndItem method [Windows Shell],IParentAndItem interface, IParentAndItem interface [Windows Shell],GetParentAndItem method, IParentAndItem.GetParentAndItem, IParentAndItem::GetParentAndItem, _shell_IParentAndItem_GetParentAndItem, shell.IParentAndItem_GetParentAndItem, shobjidl_core/IParentAndItem::GetParentAndItem
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
 - IParentAndItem::GetParentAndItem
 - shobjidl_core/IParentAndItem::GetParentAndItem
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
 - IParentAndItem.GetParentAndItem
---

# IParentAndItem::GetParentAndItem


## -description

Gets the parent of an item and the parent's child ID.

## -parameters

### -param ppidlParent [out, optional]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this method returns, contains the address of a PIDL that specifies the parent.

### -param ppsf [out, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>**</b>

When this method returns, contains the address of a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> that is the parent.

### -param ppidlChild [out, optional]

Type: <b>PITEMID_CHILD*</b>

When this method returns, contains the address of a child PIDL that identifies the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem">IParentAndItem</a> object relative to that specified by <i>ppsf</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 While <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem">IParentAndItem</a> is typically implemented on IShellItems, it is not specific to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.