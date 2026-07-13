---
UID: NF:commctrl.ListView_SetOutlineColor
title: ListView_SetOutlineColor macro (commctrl.h)
description: Sets the color of the border of a list-view control if the LVS_EX_BORDERSELECT extended window style is set. You can use this macro or send the LVM_SETOUTLINECOLOR message explicitly.
helpviewer_keywords: ["ListView_SetOutlineColor","ListView_SetOutlineColor macro [Windows Controls]","_win32_ListView_SetOutlineColor","_win32_ListView_SetOutlineColor_cpp","commctrl/ListView_SetOutlineColor","controls.ListView_SetOutlineColor","controls._win32_ListView_SetOutlineColor"]
old-location: controls\ListView_SetOutlineColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setoutlinecolor.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetOutlineColor, ListView_SetOutlineColor macro [Windows Controls], _win32_ListView_SetOutlineColor, _win32_ListView_SetOutlineColor_cpp, commctrl/ListView_SetOutlineColor, controls.ListView_SetOutlineColor, controls._win32_ListView_SetOutlineColor
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
 - ListView_SetOutlineColor
 - commctrl/ListView_SetOutlineColor
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
 - ListView_SetOutlineColor
---

# ListView_SetOutlineColor macro

## -syntax

```cpp
COLORREF ListView_SetOutlineColor(
   HWND     hwnd,
   COLORREF color
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns <b>COLORREF</b> structure that contains the outline color.


## -description

Sets the color of the border of a list-view control if the <a href="/windows/desktop/Controls/extended-list-view-styles">LVS_EX_BORDERSELECT</a> extended window style is set. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setoutlinecolor">LVM_SETOUTLINECOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param color

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

<b>COLORREF</b>

## -remarks

To use <b>ListView_SetOutlineColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
