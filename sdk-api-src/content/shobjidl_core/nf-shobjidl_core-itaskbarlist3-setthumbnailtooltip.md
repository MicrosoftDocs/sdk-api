---
UID: NF:shobjidl_core.ITaskbarList3.SetThumbnailTooltip
title: ITaskbarList3::SetThumbnailTooltip (shobjidl_core.h)
description: Specifies or updates the text of the tooltip that is displayed when the mouse pointer rests on an individual preview thumbnail in a taskbar button flyout.
helpviewer_keywords: ["ITaskbarList3 interface [Windows Shell]","SetThumbnailTooltip method","ITaskbarList3.SetThumbnailTooltip","ITaskbarList3::SetThumbnailTooltip","SetThumbnailTooltip","SetThumbnailTooltip method [Windows Shell]","SetThumbnailTooltip method [Windows Shell]","ITaskbarList3 interface","_shell_ITaskbarList3_SetThumbnailTooltip","shell.ITaskbarList3_SetThumbnailTooltip","shobjidl_core/ITaskbarList3::SetThumbnailTooltip"]
old-location: shell\ITaskbarList3_SetThumbnailTooltip.htm
tech.root: shell
ms.assetid: 73b5b9de-4876-4cac-9e58-d2e7559724f7
ms.date: 12/05/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],SetThumbnailTooltip method, ITaskbarList3.SetThumbnailTooltip, ITaskbarList3::SetThumbnailTooltip, SetThumbnailTooltip, SetThumbnailTooltip method [Windows Shell], SetThumbnailTooltip method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_SetThumbnailTooltip, shell.ITaskbarList3_SetThumbnailTooltip, shobjidl_core/ITaskbarList3::SetThumbnailTooltip
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
 - ITaskbarList3::SetThumbnailTooltip
 - shobjidl_core/ITaskbarList3::SetThumbnailTooltip
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
 - ITaskbarList3.SetThumbnailTooltip
---

# ITaskbarList3::SetThumbnailTooltip


## -description

Specifies or updates the text of the tooltip that is displayed when the mouse pointer rests on an individual preview thumbnail in a taskbar button flyout.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle to the window whose thumbnail displays the tooltip. This handle must belong to the calling process.

### -param pszTip [in]

Type: <b>LPCWSTR</b>

The pointer to the text to be displayed in the tooltip. This value can be <b>NULL</b>, in which case the title of the window specified by <i>hwnd</i> is used as the tooltip.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>