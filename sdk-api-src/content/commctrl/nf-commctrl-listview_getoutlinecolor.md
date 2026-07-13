---
UID: NF:commctrl.ListView_GetOutlineColor
title: ListView_GetOutlineColor macro (commctrl.h)
description: Gets the color of the border of a list-view control if the LVS_EX_BORDERSELECT extended window style is set. You can use this macro or send the LVM_GETOUTLINECOLOR message explicitly.
helpviewer_keywords: ["ListView_GetOutlineColor","ListView_GetOutlineColor macro [Windows Controls]","_win32_ListView_GetOutlineColor","_win32_ListView_GetOutlineColor_cpp","commctrl/ListView_GetOutlineColor","controls.ListView_GetOutlineColor","controls._win32_ListView_GetOutlineColor"]
old-location: controls\ListView_GetOutlineColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getoutlinecolor.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetOutlineColor, ListView_GetOutlineColor macro [Windows Controls], _win32_ListView_GetOutlineColor, _win32_ListView_GetOutlineColor_cpp, commctrl/ListView_GetOutlineColor, controls.ListView_GetOutlineColor, controls._win32_ListView_GetOutlineColor
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
 - ListView_GetOutlineColor
 - commctrl/ListView_GetOutlineColor
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
 - ListView_GetOutlineColor
---

# ListView_GetOutlineColor macro

## -syntax

```cpp
COLORREF ListView_GetOutlineColor(
   HWND hwnd
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns a <b>COLORREF</b> structure that contains the color of the border of a list-view control.


## -description

Gets the color of the border of a list-view control if the <a href="/windows/desktop/Controls/extended-list-view-styles">LVS_EX_BORDERSELECT</a> extended window style is set. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getoutlinecolor">LVM_GETOUTLINECOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -remarks

To use <b>ListView_GetOutlineColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
