---
UID: NF:windowsx.ListBox_GetText
title: ListBox_GetText macro (windowsx.h)
description: Gets a string from a list box. You can use this macro or send the LB_GETTEXT message explicitly.
helpviewer_keywords: ["ListBox_GetText","ListBox_GetText macro [Windows Controls]","_win32_ListBox_GetText","_win32_ListBox_GetText_cpp","controls.ListBox_GetText","controls._win32_ListBox_GetText","windowsx/ListBox_GetText"]
old-location: controls\ListBox_GetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_gettext.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetText, ListBox_GetText macro [Windows Controls], _win32_ListBox_GetText, _win32_ListBox_GetText_cpp, controls.ListBox_GetText, controls._win32_ListBox_GetText, windowsx/ListBox_GetText
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
 - ListBox_GetText
 - windowsx/ListBox_GetText
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
 - ListBox_GetText
---

# ListBox_GetText macro

## -syntax

```cpp
int ListBox_GetText(
   HWND    hwndCtl,
   int     index,
   LPCTSTR lpszBuffer
);
```

## -returns

Type: **int**

The count of characters in the string, excluding the terminating null character. If <i>index</i> does not specify a valid item, the return value is LB_ERR.


## -description

Gets a string from a list box.  You can use this macro or send the <a href="/windows/desktop/Controls/lb-gettext">LB_GETTEXT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item.

### -param lpszBuffer

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A pointer to the buffer that will receive the string. The buffer must have sufficient space for the string and a terminating null character. Before allocating the buffer, you can call <a href="/windows/desktop/api/windowsx/nf-windowsx-listbox_gettextlen">ListBox_GetTextLen</a> to retrieve the length of the string.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-gettext">LB_GETTEXT</a>.
