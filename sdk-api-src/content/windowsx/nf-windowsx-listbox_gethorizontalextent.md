---
UID: NF:windowsx.ListBox_GetHorizontalExtent
title: ListBox_GetHorizontalExtent macro (windowsx.h)
description: Gets the width that a list box can be scrolled horizontally (the scrollable width) if the list box has a horizontal scroll bar. You can use this macro or send the LB_GETHORIZONTALEXTENT message explicitly.
helpviewer_keywords: ["ListBox_GetHorizontalExtent","ListBox_GetHorizontalExtent macro [Windows Controls]","_win32_ListBox_GetHorizontalExtent","_win32_ListBox_GetHorizontalExtent_cpp","controls.ListBox_GetHorizontalExtent","controls._win32_ListBox_GetHorizontalExtent","windowsx/ListBox_GetHorizontalExtent"]
old-location: controls\ListBox_GetHorizontalExtent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_gethorizontalextent.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetHorizontalExtent, ListBox_GetHorizontalExtent macro [Windows Controls], _win32_ListBox_GetHorizontalExtent, _win32_ListBox_GetHorizontalExtent_cpp, controls.ListBox_GetHorizontalExtent, controls._win32_ListBox_GetHorizontalExtent, windowsx/ListBox_GetHorizontalExtent
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
 - ListBox_GetHorizontalExtent
 - windowsx/ListBox_GetHorizontalExtent
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
 - ListBox_GetHorizontalExtent
---

# ListBox_GetHorizontalExtent macro

## -syntax

```cpp
int ListBox_GetHorizontalExtent(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The scrollable width, in pixels, of the list box.


## -description

Gets the width that a list box can be scrolled horizontally (the scrollable width) if the list box has a horizontal scroll bar. You can use this macro or send the <a href="/windows/desktop/Controls/lb-gethorizontalextent">LB_GETHORIZONTALEXTENT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-gethorizontalextent">LB_GETHORIZONTALEXTENT</a>.
