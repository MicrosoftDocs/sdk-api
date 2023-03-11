---
UID: NF:shlobj_core.IShellFolderView.GetDragPoint
title: IShellFolderView::GetDragPoint (shlobj_core.h)
description: Gets the point at which the current drag-and-drop operation was initiated.
helpviewer_keywords: ["GetDragPoint","GetDragPoint method [Windows Shell]","GetDragPoint method [Windows Shell]","IShellFolderView interface","IShellFolderView interface [Windows Shell]","GetDragPoint method","IShellFolderView.GetDragPoint","IShellFolderView::GetDragPoint","_shell_IShellFolderView_GetDragPoint","shell.IShellFolderView_GetDragPoint","shlobj_core/IShellFolderView::GetDragPoint"]
old-location: shell\IShellFolderView_GetDragPoint.htm
tech.root: shell
ms.assetid: 6ea29e97-41cb-4de7-8320-1d6389cfb6f6
ms.date: 12/05/2018
ms.keywords: GetDragPoint, GetDragPoint method [Windows Shell], GetDragPoint method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetDragPoint method, IShellFolderView.GetDragPoint, IShellFolderView::GetDragPoint, _shell_IShellFolderView_GetDragPoint, shell.IShellFolderView_GetDragPoint, shlobj_core/IShellFolderView::GetDragPoint
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IShellFolderView::GetDragPoint
 - shlobj_core/IShellFolderView::GetDragPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.GetDragPoint
---

# IShellFolderView::GetDragPoint


## -description

<p class="CCE_Message">[This method is available through Windows Vista. It might be altered or unavailable in subsequent versions of Windows.]

Gets the point at which the current drag-and-drop operation was initiated.

## -parameters

### -param ppt [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a structure that, when this method returns successfully, receives the coordinates from which the current drag-and-drop operation was initiated.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, <b>S_FALSE</b> if the view does not have a drag point, or an error value otherwise.