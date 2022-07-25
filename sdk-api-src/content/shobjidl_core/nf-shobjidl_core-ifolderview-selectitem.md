---
UID: NF:shobjidl_core.IFolderView.SelectItem
title: IFolderView::SelectItem (shobjidl_core.h)
description: Selects an item in the folder's view.
helpviewer_keywords: ["IFolderView interface [Windows Shell]","SelectItem method","IFolderView.SelectItem","IFolderView::SelectItem","SelectItem","SelectItem method [Windows Shell]","SelectItem method [Windows Shell]","IFolderView interface","_shell_IFolderView_SelectItem","shell.IFolderView_SelectItem","shobjidl_core/IFolderView::SelectItem"]
old-location: shell\IFolderView_SelectItem.htm
tech.root: shell
ms.assetid: 6db262ea-861b-4bc5-955f-b81945313ea8
ms.date: 12/05/2018
ms.keywords: IFolderView interface [Windows Shell],SelectItem method, IFolderView.SelectItem, IFolderView::SelectItem, SelectItem, SelectItem method [Windows Shell], SelectItem method [Windows Shell],IFolderView interface, _shell_IFolderView_SelectItem, shell.IFolderView_SelectItem, shobjidl_core/IFolderView::SelectItem
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
 - IFolderView::SelectItem
 - shobjidl_core/IFolderView::SelectItem
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
 - IFolderView.SelectItem
---

# IFolderView::SelectItem


## -description

Selects an item in the folder's view.

## -parameters

### -param iItem [in]

Type: <b>int</b>

The index of the item to select in the folder's view.

### -param dwFlags [in]

Type: <b>DWORD</b>

One of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svsif">_SVSIF</a> constants that specify the type of selection to apply.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getselectionmarkeditem">IFolderView::GetSelectionMarkedItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-selectandpositionitems">IFolderView::SelectAndPositionItems</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-selectitem">SelectItem</a>