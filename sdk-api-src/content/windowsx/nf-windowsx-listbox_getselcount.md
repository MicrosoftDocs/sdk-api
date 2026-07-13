---
UID: NF:windowsx.ListBox_GetSelCount
title: ListBox_GetSelCount macro (windowsx.h)
description: Gets the count of selected items in a multiple-selection list box. You can use this macro or send the LB_GETSELCOUNT message explicitly.
helpviewer_keywords: ["ListBox_GetSelCount","ListBox_GetSelCount macro [Windows Controls]","_win32_ListBox_GetSelCount","_win32_ListBox_GetSelCount_cpp","controls.ListBox_GetSelCount","controls._win32_ListBox_GetSelCount","windowsx/ListBox_GetSelCount"]
old-location: controls\ListBox_GetSelCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getselcount.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetSelCount, ListBox_GetSelCount macro [Windows Controls], _win32_ListBox_GetSelCount, _win32_ListBox_GetSelCount_cpp, controls.ListBox_GetSelCount, controls._win32_ListBox_GetSelCount, windowsx/ListBox_GetSelCount
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
 - ListBox_GetSelCount
 - windowsx/ListBox_GetSelCount
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
 - ListBox_GetSelCount
---

# ListBox_GetSelCount macro

## -syntax

```cpp
int ListBox_GetSelCount(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The number of selected items. If the list box is a single-selection list box, the return value is LB_ERR.


## -description

Gets the count of selected items in a multiple-selection list box. You can use this macro or send the <a href="/windows/desktop/Controls/lb-getselcount">LB_GETSELCOUNT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-getselcount">LB_GETSELCOUNT</a>.
