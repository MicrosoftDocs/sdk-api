---
UID: NF:shobjidl_core.IFolderView.GetCurrentViewMode
title: IFolderView::GetCurrentViewMode (shobjidl_core.h)
description: Gets an address containing a value representing the folder's current view mode.
helpviewer_keywords: ["FVM_DETAILS","FVM_ICON","FVM_LIST","FVM_SMALLICON","FVM_THUMBNAIL","FVM_THUMBSTRIP","FVM_TILE","GetCurrentViewMode","GetCurrentViewMode method [Windows Shell]","GetCurrentViewMode method [Windows Shell]","IFolderView interface","IFolderView interface [Windows Shell]","GetCurrentViewMode method","IFolderView.GetCurrentViewMode","IFolderView::GetCurrentViewMode","_shell_IFolderView_GetCurrentViewMode","shell.IFolderView_GetCurrentViewMode","shobjidl_core/IFolderView::GetCurrentViewMode"]
old-location: shell\IFolderView_GetCurrentViewMode.htm
tech.root: shell
ms.assetid: e8f69203-f0b4-4537-980c-8e5bbdb49aab
ms.date: 12/05/2018
ms.keywords: FVM_DETAILS, FVM_ICON, FVM_LIST, FVM_SMALLICON, FVM_THUMBNAIL, FVM_THUMBSTRIP, FVM_TILE, GetCurrentViewMode, GetCurrentViewMode method [Windows Shell], GetCurrentViewMode method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetCurrentViewMode method, IFolderView.GetCurrentViewMode, IFolderView::GetCurrentViewMode, _shell_IFolderView_GetCurrentViewMode, shell.IFolderView_GetCurrentViewMode, shobjidl_core/IFolderView::GetCurrentViewMode
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
 - IFolderView::GetCurrentViewMode
 - shobjidl_core/IFolderView::GetCurrentViewMode
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
 - IFolderView.GetCurrentViewMode
---

# IFolderView::GetCurrentViewMode


## -description

Gets an address containing a value representing the folder's current view mode.

## -parameters

### -param pViewMode [out]

Type: <b>UINT*</b>

A pointer to a memory location at which to store the folder's current view mode. The value at that address is one of the following <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a> values.





#### FVM_ICON

Medium icons



#### FVM_SMALLICON

Small icons



#### FVM_LIST

List view without details



#### FVM_DETAILS

Show details (size, type, last modification date)



#### FVM_THUMBNAIL

Thumbnail view



#### FVM_TILE

Large icons



#### FVM_THUMBSTRIP

Filmstrip view

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo">GetCurrentInfo</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-setcurrentviewmode">IFolderView::SetCurrentViewMode</a>