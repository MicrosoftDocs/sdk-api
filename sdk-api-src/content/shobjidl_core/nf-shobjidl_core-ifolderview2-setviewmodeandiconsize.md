---
UID: NF:shobjidl_core.IFolderView2.SetViewModeAndIconSize
title: IFolderView2::SetViewModeAndIconSize (shobjidl_core.h)
description: Sets and applies the view mode and image size.
helpviewer_keywords: ["IFolderView2 interface [Windows Shell]","SetViewModeAndIconSize method","IFolderView2.SetViewModeAndIconSize","IFolderView2::SetViewModeAndIconSize","SetViewModeAndIconSize","SetViewModeAndIconSize method [Windows Shell]","SetViewModeAndIconSize method [Windows Shell]","IFolderView2 interface","_shell_IFolderView2_SetViewModeAndIconSize","shell.IFolderView2_SetViewModeAndIconSize","shobjidl_core/IFolderView2::SetViewModeAndIconSize"]
old-location: shell\IFolderView2_SetViewModeAndIconSize.htm
tech.root: shell
ms.assetid: 52724e5d-074f-4715-9dca-50ed22d8519e
ms.date: 12/05/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetViewModeAndIconSize method, IFolderView2.SetViewModeAndIconSize, IFolderView2::SetViewModeAndIconSize, SetViewModeAndIconSize, SetViewModeAndIconSize method [Windows Shell], SetViewModeAndIconSize method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetViewModeAndIconSize, shell.IFolderView2_SetViewModeAndIconSize, shobjidl_core/IFolderView2::SetViewModeAndIconSize
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
 - IFolderView2::SetViewModeAndIconSize
 - shobjidl_core/IFolderView2::SetViewModeAndIconSize
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
 - IFolderView2.SetViewModeAndIconSize
---

# IFolderView2::SetViewModeAndIconSize


## -description

Sets and applies the view mode and image size.

## -parameters

### -param uViewMode [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a></b>

The <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a> to be applied.

### -param iImageSize [in]

Type: <b>int</b>

The size of the image in pixels.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <i>iImageSize</i> is -1 then the current default icon size for the view mode is used.