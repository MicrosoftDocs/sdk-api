---
UID: NF:commctrl.ImageList_GetIconSize
title: ImageList_GetIconSize function (commctrl.h)
description: Retrieves the dimensions of images in an image list. All images in an image list have the same dimensions.
helpviewer_keywords: ["ImageList_GetIconSize","ImageList_GetIconSize function [Windows Controls]","_win32_ImageList_GetIconSize","_win32_ImageList_GetIconSize_cpp","commctrl/ImageList_GetIconSize","controls.ImageList_GetIconSize","controls._win32_ImageList_GetIconSize"]
old-location: controls\ImageList_GetIconSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_geticonsize.htm
ms.date: 12/05/2018
ms.keywords: ImageList_GetIconSize, ImageList_GetIconSize function [Windows Controls], _win32_ImageList_GetIconSize, _win32_ImageList_GetIconSize_cpp, commctrl/ImageList_GetIconSize, controls.ImageList_GetIconSize, controls._win32_ImageList_GetIconSize
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
 - ImageList_GetIconSize
 - commctrl/ImageList_GetIconSize
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
 - ImageList_GetIconSize
---

# ImageList_GetIconSize function


## -description

Retrieves the dimensions of images in an image list. All images in an image list have the same dimensions.

## -parameters

### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list.

### -param cx

Type: <b>int*</b>

A pointer to an integer variable that receives the width, in pixels, of each image.

### -param cy

Type: <b>int*</b>

A pointer to an integer variable that receives the height, in pixels, of each image.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.