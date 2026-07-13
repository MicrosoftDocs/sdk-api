---
UID: NF:commctrl.ListView_SetColumn
title: ListView_SetColumn macro (commctrl.h)
description: Sets the attributes of a list-view column. You can use this macro or send the LVM_SETCOLUMN message explicitly.
helpviewer_keywords: ["ListView_SetColumn","ListView_SetColumn macro [Windows Controls]","_win32_ListView_SetColumn","_win32_ListView_SetColumn_cpp","commctrl/ListView_SetColumn","controls.ListView_SetColumn","controls._win32_ListView_SetColumn"]
old-location: controls\ListView_SetColumn.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setcolumn.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetColumn, ListView_SetColumn macro [Windows Controls], _win32_ListView_SetColumn, _win32_ListView_SetColumn_cpp, commctrl/ListView_SetColumn, controls.ListView_SetColumn, controls._win32_ListView_SetColumn
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
 - ListView_SetColumn
 - commctrl/ListView_SetColumn
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
 - ListView_SetColumn
---

# ListView_SetColumn macro

## -syntax

```cpp
BOOL ListView_SetColumn(
   HWND       hwnd,
   int        iCol,
   LPLVCOLUMN pcol
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sets the attributes of a list-view column. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setcolumn">LVM_SETCOLUMN</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iCol

Type: <b>int</b>

The index of the column.

### -param pcol

Type: <b>LPLVCOLUMN</b>

A pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-lvcolumna">LVCOLUMN</a> structure that contains the new column attributes. The <b>mask</b> member specifies which column attributes to set. If the <b>mask</b> member specifies the LVCF_TEXT value, the <b>pszText</b> member is the address of a null-terminated string and the <b>cchTextMax</b> member is ignored.
