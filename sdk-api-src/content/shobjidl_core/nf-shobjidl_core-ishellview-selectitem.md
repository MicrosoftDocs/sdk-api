---
UID: NF:shobjidl_core.IShellView.SelectItem
title: IShellView::SelectItem (shobjidl_core.h)
description: Changes the selection state of one or more items within the Shell view window.
helpviewer_keywords: ["IShellView interface [Windows Shell]","SelectItem method","IShellView.SelectItem","IShellView::SelectItem","SelectItem","SelectItem method [Windows Shell]","SelectItem method [Windows Shell]","IShellView interface","_win32_IShellView_SelectItem","shell.IShellView_SelectItem","shobjidl_core/IShellView::SelectItem"]
old-location: shell\IShellView_SelectItem.htm
tech.root: shell
ms.assetid: 5c34c05e-175c-43cb-9fbb-2eb3e2b39f6f
ms.date: 12/05/2018
ms.keywords: IShellView interface [Windows Shell],SelectItem method, IShellView.SelectItem, IShellView::SelectItem, SelectItem, SelectItem method [Windows Shell], SelectItem method [Windows Shell],IShellView interface, _win32_IShellView_SelectItem, shell.IShellView_SelectItem, shobjidl_core/IShellView::SelectItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellView::SelectItem
 - shobjidl_core/IShellView::SelectItem
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
 - IShellView.SelectItem
---

# IShellView::SelectItem


## -description

Changes the selection state of one or more items within the Shell view window.

## -parameters

### -param pidlItem

Type: <b>PCUITEMID_CHILD</b>

The address of the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

### -param uFlags

Type: <b>UINT</b>

One of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svsif">_SVSIF</a> constants that specify the type of selection to apply.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method is used to implement the Target command from the <b>File</b> menu of the Shell shortcut property sheet.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>