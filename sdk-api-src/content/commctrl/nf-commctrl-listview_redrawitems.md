---
UID: NF:commctrl.ListView_RedrawItems
title: ListView_RedrawItems macro (commctrl.h)
description: Forces a list-view control to redraw a range of items. You can use this macro or send the LVM_REDRAWITEMS message explicitly.
helpviewer_keywords: ["ListView_RedrawItems","ListView_RedrawItems macro [Windows Controls]","_win32_ListView_RedrawItems","_win32_ListView_RedrawItems_cpp","commctrl/ListView_RedrawItems","controls.ListView_RedrawItems","controls._win32_ListView_RedrawItems"]
old-location: controls\ListView_RedrawItems.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_redrawitems.htm
ms.date: 10/21/2024
ms.keywords: ListView_RedrawItems, ListView_RedrawItems macro [Windows Controls], _win32_ListView_RedrawItems, _win32_ListView_RedrawItems_cpp, commctrl/ListView_RedrawItems, controls.ListView_RedrawItems, controls._win32_ListView_RedrawItems
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
 - ListView_RedrawItems
 - commctrl/ListView_RedrawItems
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
 - ListView_RedrawItems
---

# ListView_RedrawItems macro

## -syntax

```cpp
BOOL ListView_RedrawItems(
   HWND hwndLV,
   int  iFirst,
   int  iLast
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Forces a list-view control to redraw a range of items. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-redrawitems">LVM_REDRAWITEMS</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iFirst

Type: <b>int</b>

The index of the first item to redraw.

### -param iLast

Type: <b>int</b>

The index of the last item to redraw.

## -remarks

The specified items are not actually redrawn until the list-view window receives a <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message to repaint. To repaint immediately, call the <a href="/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a> function after using this macro.
