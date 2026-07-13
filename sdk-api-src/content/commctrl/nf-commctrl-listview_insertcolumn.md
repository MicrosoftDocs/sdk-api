---
UID: NF:commctrl.ListView_InsertColumn
title: ListView_InsertColumn macro (commctrl.h)
description: Inserts a new column in a list-view control. You can use this macro or send the LVM_INSERTCOLUMN message explicitly.
helpviewer_keywords: ["ListView_InsertColumn","ListView_InsertColumn macro [Windows Controls]","_win32_ListView_InsertColumn","_win32_ListView_InsertColumn_cpp","commctrl/ListView_InsertColumn","controls.ListView_InsertColumn","controls._win32_ListView_InsertColumn"]
old-location: controls\ListView_InsertColumn.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertcolumn.htm
ms.date: 10/21/2024
ms.keywords: ListView_InsertColumn, ListView_InsertColumn macro [Windows Controls], _win32_ListView_InsertColumn, _win32_ListView_InsertColumn_cpp, commctrl/ListView_InsertColumn, controls.ListView_InsertColumn, controls._win32_ListView_InsertColumn
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
 - ListView_InsertColumn
 - commctrl/ListView_InsertColumn
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
 - ListView_InsertColumn
---

# ListView_InsertColumn macro

## -syntax

```cpp
int ListView_InsertColumn(
         HWND       hwnd,
         int        iCol,
   const LPLVCOLUMN pcol
);
```

## -returns

Type: **int**

Returns the index of the new column if successful, or -1 otherwise.


## -description

Inserts a new column in a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-insertcolumn">LVM_INSERTCOLUMN</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iCol

Type: <b>int</b>

The index of the new column.

### -param pcol

Type: <b>const LPLVCOLUMN</b>

A pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-lvcolumna">LVCOLUMN</a> structure that contains the attributes of the new column.

## -remarks

Columns are visible only in report (details) view.
