---
UID: NF:shobjidl_core.ITaskbarList3.SetThumbnailClip
title: ITaskbarList3::SetThumbnailClip (shobjidl_core.h)
description: Selects a portion of a window's client area to display as that window's thumbnail in the taskbar.
helpviewer_keywords: ["ITaskbarList3 interface [Windows Shell]","SetThumbnailClip method","ITaskbarList3.SetThumbnailClip","ITaskbarList3::SetThumbnailClip","SetThumbnailClip","SetThumbnailClip method [Windows Shell]","SetThumbnailClip method [Windows Shell]","ITaskbarList3 interface","_shell_ITaskbarList3_SetThumbnailClip","shell.ITaskbarList3_SetThumbnailClip","shobjidl_core/ITaskbarList3::SetThumbnailClip"]
old-location: shell\ITaskbarList3_SetThumbnailClip.htm
tech.root: shell
ms.assetid: a22c4708-af59-4ccb-9ddb-885d14c17a33
ms.date: 12/05/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],SetThumbnailClip method, ITaskbarList3.SetThumbnailClip, ITaskbarList3::SetThumbnailClip, SetThumbnailClip, SetThumbnailClip method [Windows Shell], SetThumbnailClip method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_SetThumbnailClip, shell.ITaskbarList3_SetThumbnailClip, shobjidl_core/ITaskbarList3::SetThumbnailClip
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskbarList3::SetThumbnailClip
 - shobjidl_core/ITaskbarList3::SetThumbnailClip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3.SetThumbnailClip
---

# ITaskbarList3::SetThumbnailClip


## -description

Selects a portion of a window's client area to display as that window's thumbnail in the taskbar.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle to a window represented in the taskbar.

### -param prcClip [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies a selection within the window's client area, relative to the upper-left corner of that client area. To clear a clip that is already in place and return to the default display of the thumbnail, set this parameter to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>