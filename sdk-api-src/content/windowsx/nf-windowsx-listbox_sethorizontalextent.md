---
UID: NF:windowsx.ListBox_SetHorizontalExtent
title: ListBox_SetHorizontalExtent macro (windowsx.h)
description: Set the width by which a list box can be scrolled horizontally (the scrollable width).
helpviewer_keywords: ["ListBox_SetHorizontalExtent","ListBox_SetHorizontalExtent macro [Windows Controls]","_win32_ListBox_SetHorizontalExtent","_win32_ListBox_SetHorizontalExtent_cpp","controls.ListBox_SetHorizontalExtent","controls._win32_ListBox_SetHorizontalExtent","windowsx/ListBox_SetHorizontalExtent"]
old-location: controls\ListBox_SetHorizontalExtent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_sethorizontalextent.htm
ms.date: 10/21/2024
ms.keywords: ListBox_SetHorizontalExtent, ListBox_SetHorizontalExtent macro [Windows Controls], _win32_ListBox_SetHorizontalExtent, _win32_ListBox_SetHorizontalExtent_cpp, controls.ListBox_SetHorizontalExtent, controls._win32_ListBox_SetHorizontalExtent, windowsx/ListBox_SetHorizontalExtent
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
 - ListBox_SetHorizontalExtent
 - windowsx/ListBox_SetHorizontalExtent
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
 - ListBox_SetHorizontalExtent
---

# ListBox_SetHorizontalExtent macro

## -syntax

```cpp
void ListBox_SetHorizontalExtent(
   HWND hwndCtl,
   int  cxExtent
);
```


## -description

Set the width by which a list box can be scrolled horizontally (the scrollable width). If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box. If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden. You can use this macro or send the <a href="/windows/desktop/Controls/lb-sethorizontalextent">LB_SETHORIZONTALEXTENT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param cxExtent

Type: <b>int</b>

The number of pixels by which the list box can be scrolled.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-sethorizontalextent">LB_SETHORIZONTALEXTENT</a>.
