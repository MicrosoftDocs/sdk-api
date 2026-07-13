---
UID: NF:commctrl.ListView_SetTextBkColor
title: ListView_SetTextBkColor macro (commctrl.h)
description: Sets the background color of text in a list-view control. You can use this macro or send the LVM_SETTEXTBKCOLOR message explicitly.
helpviewer_keywords: ["ListView_SetTextBkColor","ListView_SetTextBkColor macro [Windows Controls]","_win32_ListView_SetTextBkColor","_win32_ListView_SetTextBkColor_cpp","commctrl/ListView_SetTextBkColor","controls.ListView_SetTextBkColor","controls._win32_ListView_SetTextBkColor"]
old-location: controls\ListView_SetTextBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settextbkcolor.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetTextBkColor, ListView_SetTextBkColor macro [Windows Controls], _win32_ListView_SetTextBkColor, _win32_ListView_SetTextBkColor_cpp, commctrl/ListView_SetTextBkColor, controls.ListView_SetTextBkColor, controls._win32_ListView_SetTextBkColor
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
 - ListView_SetTextBkColor
 - commctrl/ListView_SetTextBkColor
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
 - ListView_SetTextBkColor
---

# ListView_SetTextBkColor macro

## -syntax

```cpp
BOOL ListView_SetTextBkColor(
   HWND     hwnd,
   COLORREF clrTextBk
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sets the background color of text in a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-settextbkcolor">LVM_SETTEXTBKCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param clrTextBk

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The new text background color. This can be CLR_NONE for no background color.
