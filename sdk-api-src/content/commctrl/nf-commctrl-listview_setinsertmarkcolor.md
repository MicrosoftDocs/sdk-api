---
UID: NF:commctrl.ListView_SetInsertMarkColor
title: ListView_SetInsertMarkColor macro (commctrl.h)
description: Sets the color of the insertion point. You can use this macro or send the LVM_SETINSERTMARKCOLOR message explicitly.
helpviewer_keywords: ["ListView_SetInsertMarkColor","ListView_SetInsertMarkColor macro [Windows Controls]","_win32_ListView_SetInsertMarkColor","_win32_ListView_SetInsertMarkColor_cpp","commctrl/ListView_SetInsertMarkColor","controls.ListView_SetInsertMarkColor","controls._win32_ListView_SetInsertMarkColor"]
old-location: controls\ListView_SetInsertMarkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setinsertmarkcolor.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetInsertMarkColor, ListView_SetInsertMarkColor macro [Windows Controls], _win32_ListView_SetInsertMarkColor, _win32_ListView_SetInsertMarkColor_cpp, commctrl/ListView_SetInsertMarkColor, controls.ListView_SetInsertMarkColor, controls._win32_ListView_SetInsertMarkColor
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
 - ListView_SetInsertMarkColor
 - commctrl/ListView_SetInsertMarkColor
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
 - ListView_SetInsertMarkColor
---

# ListView_SetInsertMarkColor macro

## -syntax

```cpp
COLORREF ListView_SetInsertMarkColor(
   HWND     hwnd,
   COLORREF color
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns <b>COLORREF</b> structure set to the previous color.


## -description

Sets the color of the insertion point. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setinsertmarkcolor">LVM_SETINSERTMARKCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param color

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

<b>COLORREF</b>

## -remarks

To use <b>ListView_SetInsertMarkColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
