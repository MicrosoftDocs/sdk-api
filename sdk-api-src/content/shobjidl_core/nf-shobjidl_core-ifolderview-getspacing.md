---
UID: NF:shobjidl_core.IFolderView.GetSpacing
title: IFolderView::GetSpacing (shobjidl_core.h)
description: Gets a POINT structure containing the width (x) and height (y) dimensions, including the surrounding white space, of an item.
helpviewer_keywords: ["GetSpacing","GetSpacing method [Windows Shell]","GetSpacing method [Windows Shell]","IFolderView interface","IFolderView interface [Windows Shell]","GetSpacing method","IFolderView.GetSpacing","IFolderView::GetSpacing","_shell_IFolderView_GetSpacing","shell.IFolderView_GetSpacing","shobjidl_core/IFolderView::GetSpacing"]
old-location: shell\IFolderView_GetSpacing.htm
tech.root: shell
ms.assetid: 6ea81c40-773f-4f53-97c1-99619e46be48
ms.date: 12/05/2018
ms.keywords: GetSpacing, GetSpacing method [Windows Shell], GetSpacing method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetSpacing method, IFolderView.GetSpacing, IFolderView::GetSpacing, _shell_IFolderView_GetSpacing, shell.IFolderView_GetSpacing, shobjidl_core/IFolderView::GetSpacing
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
 - IFolderView::GetSpacing
 - shobjidl_core/IFolderView::GetSpacing
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
 - IFolderView.GetSpacing
---

# IFolderView::GetSpacing


## -description

Gets a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure containing the width (x) and height (y) dimensions, including the surrounding white space, of an item.

## -parameters

### -param ppt [in, out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to an existing structure to be filled with the current sizing dimensions of the items in the folder's view.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

As an example, consider an icon measuring 75 pixels by 70 pixels, with its upper-left corner located at pixel (0,0). Note that this measurement includes both the visible graphic and its surrounding buffer area. <b>IFolderView::GetSpacing</b> would return a pointer to a POINT structure containing an x value of 75 and a y value of 70. If you were using this information to avoid overlap, the next icon in line to the right would be placed with its upper-left corner at pixel (75,0). Similarly, the next icon below would be placed at pixel (0,70).

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getdefaultspacing">IFolderView::GetDefaultSpacing</a>