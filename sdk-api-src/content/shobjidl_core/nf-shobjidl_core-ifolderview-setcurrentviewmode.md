---
UID: NF:shobjidl_core.IFolderView.SetCurrentViewMode
title: IFolderView::SetCurrentViewMode (shobjidl_core.h)
description: Sets the selected folder's view mode.
helpviewer_keywords: ["FVM_DETAILS","FVM_ICON","FVM_LIST","FVM_SMALLICON","FVM_THUMBNAIL","FVM_THUMBSTRIP","FVM_TILE","IFolderView interface [Windows Shell]","SetCurrentViewMode method","IFolderView.SetCurrentViewMode","IFolderView::SetCurrentViewMode","SetCurrentViewMode","SetCurrentViewMode method [Windows Shell]","SetCurrentViewMode method [Windows Shell]","IFolderView interface","_shell_IFolderView_SetCurrentViewMode","shell.IFolderView_SetCurrentViewMode","shobjidl_core/IFolderView::SetCurrentViewMode"]
old-location: shell\IFolderView_SetCurrentViewMode.htm
tech.root: shell
ms.assetid: 7ca42567-7bb9-41e1-8f2a-5f6d0309c636
ms.date: 12/05/2018
ms.keywords: FVM_DETAILS, FVM_ICON, FVM_LIST, FVM_SMALLICON, FVM_THUMBNAIL, FVM_THUMBSTRIP, FVM_TILE, IFolderView interface [Windows Shell],SetCurrentViewMode method, IFolderView.SetCurrentViewMode, IFolderView::SetCurrentViewMode, SetCurrentViewMode, SetCurrentViewMode method [Windows Shell], SetCurrentViewMode method [Windows Shell],IFolderView interface, _shell_IFolderView_SetCurrentViewMode, shell.IFolderView_SetCurrentViewMode, shobjidl_core/IFolderView::SetCurrentViewMode
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
 - IFolderView::SetCurrentViewMode
 - shobjidl_core/IFolderView::SetCurrentViewMode
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
 - IFolderView.SetCurrentViewMode
---

# IFolderView::SetCurrentViewMode


## -description

Sets the selected folder's view mode.

## -parameters

### -param ViewMode [in]

Type: <b>UINT</b>

One of the following values from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a> enumeration.



#### FVM_ICON

Medium icons



#### FVM_SMALLICON

Small icons



#### FVM_LIST

List view without details. This view also uses small icons, but they cannot be rearranged as they can be when using <b>FVM_SMALLICON</b>.



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

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow">CreateViewWindow</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getcurrentviewmode">IFolderView::GetCurrentViewMode</a>