---
UID: NF:windowsx.ListBox_GetItemRect
title: ListBox_GetItemRect macro (windowsx.h)
description: Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box. You can use this macro or send the LB_GETITEMRECT message explicitly.
helpviewer_keywords: ["ListBox_GetItemRect","ListBox_GetItemRect macro [Windows Controls]","_win32_ListBox_GetItemRect","_win32_ListBox_GetItemRect_cpp","controls.ListBox_GetItemRect","controls._win32_ListBox_GetItemRect","windowsx/ListBox_GetItemRect"]
old-location: controls\ListBox_GetItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getitemrect.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetItemRect, ListBox_GetItemRect macro [Windows Controls], _win32_ListBox_GetItemRect, _win32_ListBox_GetItemRect_cpp, controls.ListBox_GetItemRect, controls._win32_ListBox_GetItemRect, windowsx/ListBox_GetItemRect
req.header: windowsx.h
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
 - ListBox_GetItemRect
 - windowsx/ListBox_GetItemRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ListBox_GetItemRect
---

# ListBox_GetItemRect macro

## -syntax

```cpp
int ListBox_GetItemRect(
   HWND hwndCtl,
   int  index,
   RECT *lprc
);
```

## -returns

Type: **int**

If an error occurs, the return value is LB_ERR.


## -description

Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box. You can use this macro or send the <a href="/windows/desktop/Controls/lb-getitemrect">LB_GETITEMRECT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item in the list box.

### -param lprc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the client coordinates for the item in the list box.
