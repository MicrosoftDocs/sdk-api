---
UID: NF:commctrl.ListView_SetItemPosition32
title: ListView_SetItemPosition32 macro (commctrl.h)
description: Moves an item to a specified position in a list-view control (in icon or small icon view).
helpviewer_keywords: ["ListView_SetItemPosition32","ListView_SetItemPosition32 macro [Windows Controls]","_win32_ListView_SetItemPosition32","_win32_ListView_SetItemPosition32_cpp","commctrl/ListView_SetItemPosition32","controls.ListView_SetItemPosition32","controls._win32_ListView_SetItemPosition32"]
old-location: controls\ListView_SetItemPosition32.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemposition32.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetItemPosition32, ListView_SetItemPosition32 macro [Windows Controls], _win32_ListView_SetItemPosition32, _win32_ListView_SetItemPosition32_cpp, commctrl/ListView_SetItemPosition32, controls.ListView_SetItemPosition32, controls._win32_ListView_SetItemPosition32
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
 - ListView_SetItemPosition32
 - commctrl/ListView_SetItemPosition32
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
 - ListView_SetItemPosition32
---

# ListView_SetItemPosition32 macro

## -syntax

```cpp
void ListView_SetItemPosition32(
   HWND hwndLV,
   int  i,
   int  x0,
   int  y0
);
```


## -description

Moves an item to a specified position in a list-view control (in icon or small icon view). This macro differs from the <a href="/windows/desktop/api/commctrl/nf-commctrl-listview_setitemposition">ListView_SetItemPosition</a> macro in that it uses 32-bit coordinates. You can use the <b>ListView_SetItemPosition32</b> macro or send the <a href="/windows/desktop/Controls/lvm-setitemposition32">LVM_SETITEMPOSITION32</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i

Type: <b>int</b>

The index of the list-view item for which to set the position.

### -param x0

Type: <b>int</b>

New horizontal coordinates of the item.

### -param y0

Type: <b>int</b>

New vertical coordinates of the item.

## -see-also

<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>
