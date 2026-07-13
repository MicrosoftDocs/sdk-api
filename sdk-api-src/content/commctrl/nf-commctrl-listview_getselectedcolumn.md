---
UID: NF:commctrl.ListView_GetSelectedColumn
title: ListView_GetSelectedColumn macro (commctrl.h)
description: Gets an integer that specifies the selected column. You can use this macro or send the LVM_GETSELECTEDCOLUMN message explicitly.
helpviewer_keywords: ["ListView_GetSelectedColumn","ListView_GetSelectedColumn macro [Windows Controls]","_win32_ListView_GetSelectedColumn","_win32_ListView_GetSelectedColumn_cpp","commctrl/ListView_GetSelectedColumn","controls.ListView_GetSelectedColumn","controls._win32_ListView_GetSelectedColumn"]
old-location: controls\ListView_GetSelectedColumn.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getselectedcolumn.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetSelectedColumn, ListView_GetSelectedColumn macro [Windows Controls], _win32_ListView_GetSelectedColumn, _win32_ListView_GetSelectedColumn_cpp, commctrl/ListView_GetSelectedColumn, controls.ListView_GetSelectedColumn, controls._win32_ListView_GetSelectedColumn
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
 - ListView_GetSelectedColumn
 - commctrl/ListView_GetSelectedColumn
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
 - ListView_GetSelectedColumn
---

# ListView_GetSelectedColumn macro

## -syntax

```cpp
UINT ListView_GetSelectedColumn(
   HWND hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns a <b>UINT</b> that specifies the selected column.


## -description

Gets an integer that specifies the selected column. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getselectedcolumn">LVM_GETSELECTEDCOLUMN</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -remarks

To use <b>ListView_GetSelectedColumn</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
