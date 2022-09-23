---
UID: NF:commctrl.ImageList_DragMove
title: ImageList_DragMove function (commctrl.h)
description: Moves the image that is being dragged during a drag-and-drop operation. This function is typically called in response to a WM_MOUSEMOVE message. (ImageList_DragMove)
helpviewer_keywords: ["ImageList_DragMove","ImageList_DragMove function [Windows Controls]","_win32_ImageList_DragMove","_win32_ImageList_DragMove_cpp","commctrl/ImageList_DragMove","controls.ImageList_DragMove","controls._win32_ImageList_DragMove"]
old-location: controls\ImageList_DragMove.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_dragmove.htm
ms.date: 12/05/2018
ms.keywords: ImageList_DragMove, ImageList_DragMove function [Windows Controls], _win32_ImageList_DragMove, _win32_ImageList_DragMove_cpp, commctrl/ImageList_DragMove, controls.ImageList_DragMove, controls._win32_ImageList_DragMove
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_DragMove
 - commctrl/ImageList_DragMove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_DragMove
---

# ImageList_DragMove function


## -description

Moves the image that is being dragged during a drag-and-drop operation. This function is typically called in response to a <a href="/windows/desktop/inputdev/wm-mousemove">WM_MOUSEMOVE</a> message.

## -parameters

### -param x

Type: <b>int</b>

The x-coordinate at which to display the drag image. The coordinate is relative to the upper-left corner of the window, not the client area.

### -param y

Type: <b>int</b>

The y-coordinate at which to display the drag image. The coordinate is relative to the upper-left corner of the window, not the client area.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.

## -remarks

To begin a drag operation, use the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_begindrag">ImageList_BeginDrag</a> function.
