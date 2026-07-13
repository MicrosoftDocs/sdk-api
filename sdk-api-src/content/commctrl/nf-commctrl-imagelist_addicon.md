---
UID: NF:commctrl.ImageList_AddIcon
title: ImageList_AddIcon macro (commctrl.h)
description: Adds an icon or cursor to an image list. ImageList_AddIcon calls the ImageList_ReplaceIcon function.
helpviewer_keywords: ["ImageList_AddIcon","ImageList_AddIcon macro [Windows Controls]","_win32_ImageList_AddIcon","_win32_ImageList_AddIcon_cpp","commctrl/ImageList_AddIcon","controls.ImageList_AddIcon","controls._win32_ImageList_AddIcon"]
old-location: controls\ImageList_AddIcon.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\macros\imagelist_addicon.htm
ms.date: 10/21/2024
ms.keywords: ImageList_AddIcon, ImageList_AddIcon macro [Windows Controls], _win32_ImageList_AddIcon, _win32_ImageList_AddIcon_cpp, commctrl/ImageList_AddIcon, controls.ImageList_AddIcon, controls._win32_ImageList_AddIcon
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
 - ImageList_AddIcon
 - commctrl/ImageList_AddIcon
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
 - ImageList_AddIcon
---

# ImageList_AddIcon macro

## -syntax

```cpp
int ImageList_AddIcon(
   HIMAGELIST himl,
   HICON      hicon
);
```


## -description

Adds an icon or cursor to an image list. <b>ImageList_AddIcon</b> calls the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_replaceicon">ImageList_ReplaceIcon</a> function.

## -parameters

### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list. If this parameter identifies a masked image list, the macro copies both the image and mask bitmaps of the icon or cursor. If this parameter identifies a nonmasked image list, the macro copies only the image bitmap.

### -param hicon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HICON</a></b>

A handle to the icon or cursor that contains the bitmap and mask for the new image.

## -returns

Type: <b>int</b>

Returns the index of the image if successful, or -1 otherwise.

## -remarks

Because the system does not save 
				<i>hicon</i>, you can destroy it after the macro returns if the icon or cursor was created by the <a href="/windows/desktop/api/winuser/nf-winuser-createicon">CreateIcon</a> function. You do not need to destroy <i>hicon</i> if it was loaded by the <a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a> function; the system automatically frees an icon resource when it is no longer needed. 

The <b>ImageList_AddIcon</b> macro is defined as follows: 


``` syntax
#define  ImageList_AddIcon(himl, hicon) ImageList_ReplaceIcon(himl, -1, hicon)
```

