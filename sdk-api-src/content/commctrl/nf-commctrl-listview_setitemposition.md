---
UID: NF:commctrl.ListView_SetItemPosition
title: ListView_SetItemPosition macro (commctrl.h)
description: Moves an item to a specified position in a list-view control (in icon or small icon view). You can use this macro or send the LVM_SETITEMPOSITION message explicitly.
helpviewer_keywords: ["ListView_SetItemPosition","ListView_SetItemPosition macro [Windows Controls]","_win32_ListView_SetItemPosition","_win32_ListView_SetItemPosition_cpp","commctrl/ListView_SetItemPosition","controls.ListView_SetItemPosition","controls._win32_ListView_SetItemPosition"]
old-location: controls\ListView_SetItemPosition.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemposition.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetItemPosition, ListView_SetItemPosition macro [Windows Controls], _win32_ListView_SetItemPosition, _win32_ListView_SetItemPosition_cpp, commctrl/ListView_SetItemPosition, controls.ListView_SetItemPosition, controls._win32_ListView_SetItemPosition
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
 - ListView_SetItemPosition
 - commctrl/ListView_SetItemPosition
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
 - ListView_SetItemPosition
---

# ListView_SetItemPosition macro

## -syntax

```cpp
BOOL ListView_SetItemPosition(
   HWND hwndLV,
   int  i,
   int  x,
   int  y
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Moves an item to a specified position in a list-view control (in icon or small icon view). You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setitemposition">LVM_SETITEMPOSITION</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i

Type: <b>int</b>

The index of the list-view item.

### -param x

Type: <b>int</b>

The new x-position of the item's upper-left corner, in view coordinates.

### -param y

Type: <b>int</b>

The new y-position of the item's upper-left corner, in view coordinates.

## -remarks

If the list-view control has the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_AUTOARRANGE</a> style, the list-view control is arranged after the position of the item is set. 

On Windows Vista, calling this macro on a list-view control with the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_AUTOARRANGE</a> style does nothing, and the return value is <b>FALSE</b>.
