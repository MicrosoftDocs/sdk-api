---
UID: NF:commctrl.Header_GetStateImageList
title: Header_GetStateImageList macro (commctrl.h)
description: Gets the handle to the image list that has been set for an existing header control state.
helpviewer_keywords: ["Header_GetStateImageList","Header_GetStateImageList macro [Windows Controls]","_win32_Header_GetStateImageList","_win32_Header_GetStateImageList_cpp","commctrl/Header_GetStateImageList","controls.Header_GetStateImageList","controls._win32_Header_GetStateImageList"]
old-location: controls\Header_GetStateImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getstateimagelist.htm
ms.date: 10/21/2024
ms.keywords: Header_GetStateImageList, Header_GetStateImageList macro [Windows Controls], _win32_Header_GetStateImageList, _win32_Header_GetStateImageList_cpp, commctrl/Header_GetStateImageList, controls.Header_GetStateImageList, controls._win32_Header_GetStateImageList
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
 - Header_GetStateImageList
 - commctrl/Header_GetStateImageList
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
 - Header_GetStateImageList
---

# Header_GetStateImageList macro

## -syntax

```cpp
BOOL Header_GetStateImageList(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the image list that is set for the header control state.


## -description

Gets the handle to the image list that has been set for an existing header control state.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control.
