---
UID: NF:shobjidl_core.IFolderView.Item
title: IFolderView::Item (shobjidl_core.h)
description: Gets the identifier of a specific item in the folder view, by index.
helpviewer_keywords: ["IFolderView interface [Windows Shell]","Item method","IFolderView.Item","IFolderView::Item","Item","Item method [Windows Shell]","Item method [Windows Shell]","IFolderView interface","_shell_IFolderView_Item","shell.IFolderView_Item","shobjidl_core/IFolderView::Item"]
old-location: shell\IFolderView_Item.htm
tech.root: shell
ms.assetid: c130ef36-1255-4c57-be31-7fc2029d9f66
ms.date: 12/05/2018
ms.keywords: IFolderView interface [Windows Shell],Item method, IFolderView.Item, IFolderView::Item, Item, Item method [Windows Shell], Item method [Windows Shell],IFolderView interface, _shell_IFolderView_Item, shell.IFolderView_Item, shobjidl_core/IFolderView::Item
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderView::Item
 - shobjidl_core/IFolderView::Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFolderView.Item
---

# IFolderView::Item


## -description

Gets the identifier of a specific item in the folder view, by index.

## -parameters

### -param iItemIndex [in]

Type: <b>int</b>

The index of the item in the view.

### -param ppidl [out]

Type: <b>PITEMID_CHILD*</b>

The address of a pointer to a PIDL containing the item's identifier information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When no longer needed, the PIDL should be freed by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-items">IFolderView::Items</a>