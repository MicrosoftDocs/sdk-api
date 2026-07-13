---
UID: NF:commctrl.ImageList_GetDragImage
title: ImageList_GetDragImage function (commctrl.h)
description: Retrieves the temporary image list that is used for the drag image. The function also retrieves the current drag position and the offset of the drag image relative to the drag position.
helpviewer_keywords: ["ImageList_GetDragImage","ImageList_GetDragImage function [Windows Controls]","_win32_ImageList_GetDragImage","_win32_ImageList_GetDragImage_cpp","commctrl/ImageList_GetDragImage","controls.ImageList_GetDragImage","controls._win32_ImageList_GetDragImage"]
old-location: controls\ImageList_GetDragImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_getdragimage.htm
ms.date: 12/05/2018
ms.keywords: ImageList_GetDragImage, ImageList_GetDragImage function [Windows Controls], _win32_ImageList_GetDragImage, _win32_ImageList_GetDragImage_cpp, commctrl/ImageList_GetDragImage, controls.ImageList_GetDragImage, controls._win32_ImageList_GetDragImage
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
 - ImageList_GetDragImage
 - commctrl/ImageList_GetDragImage
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
 - ImageList_GetDragImage
---

# ImageList_GetDragImage function


## -description

Retrieves the temporary image list that is used for the drag image. The function also retrieves the current drag position and the offset of the drag image relative to the drag position.

## -parameters

### -param ppt

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the current drag position. Can be <b>NULL</b>.

### -param pptHotspot

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a <b>POINT</b> structure that receives the offset of the drag image relative to the drag position. Can be <b>NULL</b>.

## -returns

Type: <b>HIMAGELIST</b>

Returns the handle to the image list if successful, or <b>NULL</b> otherwise.

## -remarks

The temporary image list is destroyed when the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_enddrag">ImageList_EndDrag</a> function is called. To begin a drag operation, use the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_begindrag">ImageList_BeginDrag</a> function.