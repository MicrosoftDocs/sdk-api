---
UID: NF:commctrl.ListView_CreateDragImage
title: ListView_CreateDragImage macro (commctrl.h)
description: Creates a drag image list for the specified item. You can use this macro or send the LVM_CREATEDRAGIMAGE message explicitly.
helpviewer_keywords: ["ListView_CreateDragImage","ListView_CreateDragImage macro [Windows Controls]","_win32_ListView_CreateDragImage","_win32_ListView_CreateDragImage_cpp","commctrl/ListView_CreateDragImage","controls.ListView_CreateDragImage","controls._win32_ListView_CreateDragImage"]
old-location: controls\ListView_CreateDragImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_createdragimage.htm
ms.date: 10/21/2024
ms.keywords: ListView_CreateDragImage, ListView_CreateDragImage macro [Windows Controls], _win32_ListView_CreateDragImage, _win32_ListView_CreateDragImage_cpp, commctrl/ListView_CreateDragImage, controls.ListView_CreateDragImage, controls._win32_ListView_CreateDragImage
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
 - ListView_CreateDragImage
 - commctrl/ListView_CreateDragImage
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
 - ListView_CreateDragImage
---

# ListView_CreateDragImage macro

## -syntax

```cpp
HIMAGELIST ListView_CreateDragImage(
   HWND    hwnd,
   int     i,
   LPPOINT lpptUpLeft
);
```

## -returns

Type: **HIMAGELIST**

Returns the handle to the drag image list if successful, or <b>NULL</b> otherwise.


## -description

Creates a drag image list for the specified item. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-createdragimage">LVM_CREATEDRAGIMAGE</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i

Type: <b>int</b>

The index of the item.

### -param lpptUpLeft

Type: <b>LPPOINT</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the initial location of the upper-left corner of the image, in view coordinates.

## -remarks

Your application is responsible for destroying the image list when it is no longer needed.
