---
UID: NF:shobjidl_core.IFolderView.GetSelectionMarkedItem
title: IFolderView::GetSelectionMarkedItem (shobjidl_core.h)
description: Gets the index of an item in the folder's view which has been marked by using the SVSI_SELECTIONMARK in IFolderView::SelectItem.
helpviewer_keywords: ["GetSelectionMarkedItem","GetSelectionMarkedItem method [Windows Shell]","GetSelectionMarkedItem method [Windows Shell]","IFolderView interface","IFolderView interface [Windows Shell]","GetSelectionMarkedItem method","IFolderView.GetSelectionMarkedItem","IFolderView::GetSelectionMarkedItem","_shell_IFolderView_GetSelectionMarkedItem","shell.IFolderView_GetSelectionMarkedItem","shobjidl_core/IFolderView::GetSelectionMarkedItem"]
old-location: shell\IFolderView_GetSelectionMarkedItem.htm
tech.root: shell
ms.assetid: 86416704-c2e3-4782-a566-b49cbd0e7696
ms.date: 12/05/2018
ms.keywords: GetSelectionMarkedItem, GetSelectionMarkedItem method [Windows Shell], GetSelectionMarkedItem method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetSelectionMarkedItem method, IFolderView.GetSelectionMarkedItem, IFolderView::GetSelectionMarkedItem, _shell_IFolderView_GetSelectionMarkedItem, shell.IFolderView_GetSelectionMarkedItem, shobjidl_core/IFolderView::GetSelectionMarkedItem
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
 - IFolderView::GetSelectionMarkedItem
 - shobjidl_core/IFolderView::GetSelectionMarkedItem
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
 - IFolderView.GetSelectionMarkedItem
---

# IFolderView::GetSelectionMarkedItem


## -description

Gets the index of an item in the folder's view which has been marked by using the SVSI_SELECTIONMARK in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-selectitem">IFolderView::SelectItem</a>.

## -parameters

### -param piItem [out]

Type: <b>int*</b>

A pointer to the index of the marked item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-selectitem">IFolderView::SelectItem</a>