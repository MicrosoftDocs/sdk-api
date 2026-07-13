---
UID: NF:commctrl.ImageList_ExtractIcon
title: ImageList_ExtractIcon macro (commctrl.h)
description: Calls the ImageList_GetIcon function to create an icon or cursor based on an image and mask in an image list.
helpviewer_keywords: ["ImageList_ExtractIcon","ImageList_ExtractIcon macro [Windows Controls]","_win32_ImageList_ExtractIcon","_win32_ImageList_ExtractIcon_cpp","commctrl/ImageList_ExtractIcon","controls.ImageList_ExtractIcon","controls._win32_ImageList_ExtractIcon"]
old-location: controls\ImageList_ExtractIcon.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\macros\imagelist_extracticon.htm
ms.date: 10/21/2024
ms.keywords: ImageList_ExtractIcon, ImageList_ExtractIcon macro [Windows Controls], _win32_ImageList_ExtractIcon, _win32_ImageList_ExtractIcon_cpp, commctrl/ImageList_ExtractIcon, controls.ImageList_ExtractIcon, controls._win32_ImageList_ExtractIcon
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
 - ImageList_ExtractIcon
 - commctrl/ImageList_ExtractIcon
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
 - ImageList_ExtractIcon
---

# ImageList_ExtractIcon macro

## -syntax

```cpp
HICON ImageList_ExtractIcon(
   HINSTANCE  hi,
   HIMAGELIST himl,
   int        i
);
```

## -returns

Type: **[HICON](/windows/desktop/winprog/windows-data-types)**

Returns the handle of the icon or cursor if successful, or <b>NULL</b> otherwise.


## -description

Calls the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_geticon">ImageList_GetIcon</a> function to create an icon or cursor based on an image and mask in an image list.

## -parameters

### -param hi

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

This parameter is not used and should always be zero.

### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list.

### -param i

Type: <b>int</b>

The index of the image.

## -remarks

It is the responsibility of the calling application to destroy the icon returned from this function by using the <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> function.
