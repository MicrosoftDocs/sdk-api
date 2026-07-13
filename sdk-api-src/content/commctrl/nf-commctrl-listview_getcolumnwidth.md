---
UID: NF:commctrl.ListView_GetColumnWidth
title: ListView_GetColumnWidth macro (commctrl.h)
description: Gets the width of a column in report or list view. You can use this macro or send the LVM_GETCOLUMNWIDTH message explicitly.
helpviewer_keywords: ["ListView_GetColumnWidth","ListView_GetColumnWidth macro [Windows Controls]","_win32_ListView_GetColumnWidth","_win32_ListView_GetColumnWidth_cpp","commctrl/ListView_GetColumnWidth","controls.ListView_GetColumnWidth","controls._win32_ListView_GetColumnWidth"]
old-location: controls\ListView_GetColumnWidth.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcolumnwidth.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetColumnWidth, ListView_GetColumnWidth macro [Windows Controls], _win32_ListView_GetColumnWidth, _win32_ListView_GetColumnWidth_cpp, commctrl/ListView_GetColumnWidth, controls.ListView_GetColumnWidth, controls._win32_ListView_GetColumnWidth
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
 - ListView_GetColumnWidth
 - commctrl/ListView_GetColumnWidth
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
 - ListView_GetColumnWidth
---

# ListView_GetColumnWidth macro

## -syntax

```cpp
int ListView_GetColumnWidth(
   HWND hwnd,
   int  iCol
);
```

## -returns

Type: **int**

Returns the column width if successful, or zero otherwise. If this macro is used on a list-view control with the <b>LVS_REPORT</b> style and the specified column does not exist, the return value is undefined.


## -description

Gets the width of a column in report or list view. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getcolumnwidth">LVM_GETCOLUMNWIDTH</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iCol

Type: <b>int</b>

The index of the column. This parameter is ignored in list view.
