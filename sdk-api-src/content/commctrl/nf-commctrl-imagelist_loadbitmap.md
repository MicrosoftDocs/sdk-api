---
UID: NF:commctrl.ImageList_LoadBitmap
title: ImageList_LoadBitmap macro (commctrl.h)
description: Calls the ImageList_LoadImage function to create an image list from the specified bitmap resource.
helpviewer_keywords: ["ImageList_LoadBitmap","ImageList_LoadBitmap macro [Windows Controls]","_win32_ImageList_LoadBitmap","_win32_ImageList_LoadBitmap_cpp","commctrl/ImageList_LoadBitmap","controls.ImageList_LoadBitmap","controls._win32_ImageList_LoadBitmap"]
old-location: controls\ImageList_LoadBitmap.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\macros\imagelist_loadbitmap.htm
ms.date: 10/21/2024
ms.keywords: ImageList_LoadBitmap, ImageList_LoadBitmap macro [Windows Controls], _win32_ImageList_LoadBitmap, _win32_ImageList_LoadBitmap_cpp, commctrl/ImageList_LoadBitmap, controls.ImageList_LoadBitmap, controls._win32_ImageList_LoadBitmap
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_LoadBitmap
 - commctrl/ImageList_LoadBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ImageList_LoadBitmap
---

# ImageList_LoadBitmap macro

## -syntax

```cpp
HIMAGELIST ImageList_LoadBitmap(
   HINSTANCE hi,
   LPCTSTR   lpbmp,
   int       cx,
   int       cGrow,
   COLORREF  crMask
);
```

## -returns

Type: **HIMAGELIST**

Returns the handle to the image list if successful, or <b>NULL</b> otherwise.


## -description

Calls the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_loadimagea">ImageList_LoadImage</a> function to create an image list from the specified bitmap resource.

## -parameters

### -param hi

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

A handle to the instance that contains the bitmap resource. This parameter is <b>NULL</b> if you are loading an OEM bitmap.

### -param lpbmp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The image to load. If the <i>hi</i> parameter is non-<b>NULL</b>, <i>lpbmp</i> is the address of a null-terminated string that contains the name of the image resource in the <i>hi</i> module. If <i>hi</i> is <b>NULL</b>, the <a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> of this parameter must be the identifier of an OEM bitmap to load. To create this value, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro with one of the OEM bitmap identifiers defined in WINUSER.H. These identifiers have the OBM_ prefix.

### -param cx

Type: <b>int</b>

The width of each image. The height of each image and the initial number of images are inferred by the dimensions of the specified bitmap.

### -param cGrow

Type: <b>int</b>

The number of images by which the image list can grow when the system needs to make room for new images. This parameter represents the number of new images that the resized image list can contain.

### -param crMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The color used to generate a mask. Each pixel of this color in the specified bitmap is changed to black, and the corresponding bit in the mask is set to 1. If this parameter is the CLR_NONE value, no mask is generated.
