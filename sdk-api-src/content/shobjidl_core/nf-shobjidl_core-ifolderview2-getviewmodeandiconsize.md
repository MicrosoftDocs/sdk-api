---
UID: NF:shobjidl_core.IFolderView2.GetViewModeAndIconSize
title: IFolderView2::GetViewModeAndIconSize (shobjidl_core.h)
description: Gets the current view mode and icon size applied to the view.
helpviewer_keywords: ["GetViewModeAndIconSize","GetViewModeAndIconSize method [Windows Shell]","GetViewModeAndIconSize method [Windows Shell]","IFolderView2 interface","IFolderView2 interface [Windows Shell]","GetViewModeAndIconSize method","IFolderView2.GetViewModeAndIconSize","IFolderView2::GetViewModeAndIconSize","_shell_IFolderView2_GetViewModeAndIconSize","shell.IFolderView2_GetViewModeAndIconSize","shobjidl_core/IFolderView2::GetViewModeAndIconSize"]
old-location: shell\IFolderView2_GetViewModeAndIconSize.htm
tech.root: shell
ms.assetid: 4696d55e-aad7-41f2-b2c0-47d4b507c70c
ms.date: 12/05/2018
ms.keywords: GetViewModeAndIconSize, GetViewModeAndIconSize method [Windows Shell], GetViewModeAndIconSize method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetViewModeAndIconSize method, IFolderView2.GetViewModeAndIconSize, IFolderView2::GetViewModeAndIconSize, _shell_IFolderView2_GetViewModeAndIconSize, shell.IFolderView2_GetViewModeAndIconSize, shobjidl_core/IFolderView2::GetViewModeAndIconSize
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
 - IFolderView2::GetViewModeAndIconSize
 - shobjidl_core/IFolderView2::GetViewModeAndIconSize
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
 - IFolderView2.GetViewModeAndIconSize
---

# IFolderView2::GetViewModeAndIconSize


## -description

Gets the current view mode and icon size applied to the view.

## -parameters

### -param puViewMode [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a>*</b>

A pointer to the current <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a>.

### -param piImageSize [out]

Type: <b>int*</b>

A pointer to the size of the icon in pixels.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.