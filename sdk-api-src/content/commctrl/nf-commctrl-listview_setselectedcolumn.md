---
UID: NF:commctrl.ListView_SetSelectedColumn
title: ListView_SetSelectedColumn macro (commctrl.h)
description: Sets the index of the selected column. You can use this macro or send the LVM_SETSELECTEDCOLUMN message explicitly.
helpviewer_keywords: ["ListView_SetSelectedColumn","ListView_SetSelectedColumn macro [Windows Controls]","_win32_ListView_SetSelectedColumn","_win32_ListView_SetSelectedColumn_cpp","commctrl/ListView_SetSelectedColumn","controls.ListView_SetSelectedColumn","controls._win32_ListView_SetSelectedColumn"]
old-location: controls\ListView_SetSelectedColumn.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setselectedcolumn.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetSelectedColumn, ListView_SetSelectedColumn macro [Windows Controls], _win32_ListView_SetSelectedColumn, _win32_ListView_SetSelectedColumn_cpp, commctrl/ListView_SetSelectedColumn, controls.ListView_SetSelectedColumn, controls._win32_ListView_SetSelectedColumn
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
 - ListView_SetSelectedColumn
 - commctrl/ListView_SetSelectedColumn
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
 - ListView_SetSelectedColumn
---

# ListView_SetSelectedColumn macro

## -syntax

```cpp
void ListView_SetSelectedColumn(
   HWND hwnd,
   int  iCol
);
```


## -description

Sets the index of the selected column. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setselectedcolumn">LVM_SETSELECTEDCOLUMN</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iCol

Type: <b>int</b>

<b>int</b>

## -remarks

To use <b>ListView_SetSelectedColumn</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
