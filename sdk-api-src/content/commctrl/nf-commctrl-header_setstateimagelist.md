---
UID: NF:commctrl.Header_SetStateImageList
title: Header_SetStateImageList macro (commctrl.h)
description: Assigns an image list to an existing header control state.
helpviewer_keywords: ["Header_SetStateImageList","Header_SetStateImageList macro [Windows Controls]","_win32_Header_SetStateImageList","_win32_Header_SetStateImageList_cpp","commctrl/Header_SetStateImageList","controls.Header_SetStateImageList","controls._win32_Header_SetStateImageList"]
old-location: controls\Header_SetStateImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setstateimagelist.htm
ms.date: 10/21/2024
ms.keywords: Header_SetStateImageList, Header_SetStateImageList macro [Windows Controls], _win32_Header_SetStateImageList, _win32_Header_SetStateImageList_cpp, commctrl/Header_SetStateImageList, controls.Header_SetStateImageList, controls._win32_Header_SetStateImageList
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Header_SetStateImageList
 - commctrl/Header_SetStateImageList
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
 - Header_SetStateImageList
---

# Header_SetStateImageList macro

## -syntax

```cpp
BOOL Header_SetStateImageList(
   HWND       hwnd,
   HIMAGELIST himl
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the image list previously assigned to the header control state, or <b>NULL</b> if there is no previous image list.


## -description

Assigns an image list to an existing header control state.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control.

### -param himl

Type: <b>HIMAGELIST</b>

A handle to an image list control.
