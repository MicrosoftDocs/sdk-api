---
UID: NF:windowsx.ListBox_GetTopIndex
title: ListBox_GetTopIndex macro (windowsx.h)
description: Gets the index of the first visible item in a list box. You can use this macro or send the LB_GETTOPINDEX message explicitly.
helpviewer_keywords: ["ListBox_GetTopIndex","ListBox_GetTopIndex macro [Windows Controls]","_win32_ListBox_GetTopIndex","_win32_ListBox_GetTopIndex_cpp","controls.ListBox_GetTopIndex","controls._win32_ListBox_GetTopIndex","windowsx/ListBox_GetTopIndex"]
old-location: controls\ListBox_GetTopIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_gettopindex.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetTopIndex, ListBox_GetTopIndex macro [Windows Controls], _win32_ListBox_GetTopIndex, _win32_ListBox_GetTopIndex_cpp, controls.ListBox_GetTopIndex, controls._win32_ListBox_GetTopIndex, windowsx/ListBox_GetTopIndex
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
 - ListBox_GetTopIndex
 - windowsx/ListBox_GetTopIndex
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
 - ListBox_GetTopIndex
---

# ListBox_GetTopIndex macro

## -syntax

```cpp
int ListBox_GetTopIndex(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The zero-based index of the first visible item.


## -description

Gets the index of the first visible item in a list box. You can use this macro or send the <a href="/windows/desktop/controls/lb-gettopindex">LB_GETTOPINDEX</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.
