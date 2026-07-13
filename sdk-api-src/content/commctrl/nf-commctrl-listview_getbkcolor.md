---
UID: NF:commctrl.ListView_GetBkColor
title: ListView_GetBkColor macro (commctrl.h)
description: Gets the background color of a list-view control. You can use this macro or send the LVM_GETBKCOLOR message explicitly.
helpviewer_keywords: ["ListView_GetBkColor","ListView_GetBkColor macro [Windows Controls]","_win32_ListView_GetBkColor","_win32_ListView_GetBkColor_cpp","commctrl/ListView_GetBkColor","controls.ListView_GetBkColor","controls._win32_ListView_GetBkColor"]
old-location: controls\ListView_GetBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getbkcolor.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetBkColor, ListView_GetBkColor macro [Windows Controls], _win32_ListView_GetBkColor, _win32_ListView_GetBkColor_cpp, commctrl/ListView_GetBkColor, controls.ListView_GetBkColor, controls._win32_ListView_GetBkColor
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
 - ListView_GetBkColor
 - commctrl/ListView_GetBkColor
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
 - ListView_GetBkColor
---

# ListView_GetBkColor macro

## -syntax

```cpp
COLORREF ListView_GetBkColor(
   HWND hwnd
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns the background color of the list-view control.


## -description

Gets the background color of a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getbkcolor">LVM_GETBKCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.
