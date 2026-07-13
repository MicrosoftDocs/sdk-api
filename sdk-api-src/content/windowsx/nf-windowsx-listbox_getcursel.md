---
UID: NF:windowsx.ListBox_GetCurSel
title: ListBox_GetCurSel macro (windowsx.h)
description: Gets the index of the currently selected item in a single-selection list box. You can use this macro or send the LB_GETCURSEL message explicitly.
helpviewer_keywords: ["ListBox_GetCurSel","ListBox_GetCurSel macro [Windows Controls]","_win32_ListBox_GetCurSel","_win32_ListBox_GetCurSel_cpp","controls.ListBox_GetCurSel","controls._win32_ListBox_GetCurSel","windowsx/ListBox_GetCurSel"]
old-location: controls\ListBox_GetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getcursel.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetCurSel, ListBox_GetCurSel macro [Windows Controls], _win32_ListBox_GetCurSel, _win32_ListBox_GetCurSel_cpp, controls.ListBox_GetCurSel, controls._win32_ListBox_GetCurSel, windowsx/ListBox_GetCurSel
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
 - ListBox_GetCurSel
 - windowsx/ListBox_GetCurSel
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
 - ListBox_GetCurSel
---

# ListBox_GetCurSel macro

## -syntax

```cpp
int ListBox_GetCurSel(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The zero-based index of the selected item. If there is no selection, the return value is LB_ERR.


## -description

Gets the index of the currently selected item in a single-selection list box. You can use this macro or send the <a href="/windows/desktop/Controls/lb-getcursel">LB_GETCURSEL</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-getcursel">LB_GETCURSEL</a>.
