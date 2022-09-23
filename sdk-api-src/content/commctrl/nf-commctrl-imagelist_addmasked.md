---
UID: NF:commctrl.ImageList_AddMasked
title: ImageList_AddMasked function (commctrl.h)
description: Adds an image or images to an image list, generating a mask from the specified bitmap. (ImageList_AddMasked)
helpviewer_keywords: ["ImageList_AddMasked","ImageList_AddMasked function [Windows Controls]","_win32_ImageList_AddMasked","_win32_ImageList_AddMasked_cpp","commctrl/ImageList_AddMasked","controls.ImageList_AddMasked","controls._win32_ImageList_AddMasked"]
old-location: controls\ImageList_AddMasked.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_addmasked.htm
ms.date: 12/05/2018
ms.keywords: ImageList_AddMasked, ImageList_AddMasked function [Windows Controls], _win32_ImageList_AddMasked, _win32_ImageList_AddMasked_cpp, commctrl/ImageList_AddMasked, controls.ImageList_AddMasked, controls._win32_ImageList_AddMasked
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
 - ImageList_AddMasked
 - commctrl/ImageList_AddMasked
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
 - Ext-MS-Win-Shell-ComCtl32-Init-L1-1-1.dll
api_name:
 - ImageList_AddMasked
req.apiset: ext-ms-win-shell-comctl32-init-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# ImageList_AddMasked function


## -description

Adds an image or images to an image list, generating a mask from the specified bitmap.

## -parameters

### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list.

### -param hbmImage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

A handle to the bitmap that contains one or more images. The number of images is inferred from the width of the bitmap.

### -param crMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The color used to generate the mask. Each pixel of this color in the specified bitmap is changed to black, and the corresponding bit in the mask is set to 1. If this parameter is CLR_DEFAULT, then the color of the pixel at (0,0) is used as the mask.

## -returns

Type: <b>int</b>

Returns the index of the first new image if successful, or -1 otherwise.

## -remarks

The <b>ImageList_AddMasked</b> function copies the bitmap to an internal data structure. Bitmaps with color depth greater than 8bpp are not supported. Be sure to use the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete <i>hbmImage</i> after the function returns.
