---
UID: NF:commctrl.ImageList_DragEnter
title: ImageList_DragEnter function (commctrl.h)
description: Displays the drag image at the specified position within the window.
helpviewer_keywords: ["ImageList_DragEnter","ImageList_DragEnter function [Windows Controls]","_win32_ImageList_DragEnter","_win32_ImageList_DragEnter_cpp","commctrl/ImageList_DragEnter","controls.ImageList_DragEnter","controls._win32_ImageList_DragEnter"]
old-location: controls\ImageList_DragEnter.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_dragenter.htm
ms.date: 12/05/2018
ms.keywords: ImageList_DragEnter, ImageList_DragEnter function [Windows Controls], _win32_ImageList_DragEnter, _win32_ImageList_DragEnter_cpp, commctrl/ImageList_DragEnter, controls.ImageList_DragEnter, controls._win32_ImageList_DragEnter
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
 - ImageList_DragEnter
 - commctrl/ImageList_DragEnter
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
 - ImageList_DragEnter
---

# ImageList_DragEnter function


## -description

Displays the drag image at the specified position within the window.

## -parameters

### -param hwndLock

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that owns the drag image.

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