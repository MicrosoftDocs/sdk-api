---
UID: NF:commctrl.ImageList_BeginDrag
title: ImageList_BeginDrag function (commctrl.h)
description: Begins dragging an image. (ImageList_BeginDrag)
helpviewer_keywords: ["ImageList_BeginDrag","ImageList_BeginDrag function [Windows Controls]","_win32_ImageList_BeginDrag","_win32_ImageList_BeginDrag_cpp","commctrl/ImageList_BeginDrag","controls.ImageList_BeginDrag","controls._win32_ImageList_BeginDrag"]
old-location: controls\ImageList_BeginDrag.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_begindrag.htm
ms.date: 12/05/2018
ms.keywords: ImageList_BeginDrag, ImageList_BeginDrag function [Windows Controls], _win32_ImageList_BeginDrag, _win32_ImageList_BeginDrag_cpp, commctrl/ImageList_BeginDrag, controls.ImageList_BeginDrag, controls._win32_ImageList_BeginDrag
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
 - ImageList_BeginDrag
 - commctrl/ImageList_BeginDrag
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
 - ImageList_BeginDrag
---

# ImageList_BeginDrag function


## -description

Begins dragging an image.

## -parameters

### -param himlTrack

Type: <b>HIMAGELIST</b>

A handle to the image list.

### -param iTrack

Type: <b>int</b>

The index of the image to drag.

### -param dxHotspot

Type: <b>int</b>

The x-coordinate of the location of the drag position relative to the upper-left corner of the image.

### -param dyHotspot

Type: <b>int</b>

The y-coordinate of the location of the drag position relative to the upper-left corner of the image.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.

## -remarks

This function creates a temporary image list that is used for dragging. In response to subsequent <a href="/windows/desktop/inputdev/wm-mousemove">WM_MOUSEMOVE</a> messages, you can move the drag image by using the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_dragmove">ImageList_DragMove</a> function. To end the drag operation, you can use the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_enddrag">ImageList_EndDrag</a> function.
