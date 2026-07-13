---
UID: NF:commctrl.ListView_SetTextColor
title: ListView_SetTextColor macro (commctrl.h)
description: Sets the text color of a list-view control. You can use this macro or send the LVM_SETTEXTCOLOR message explicitly.
helpviewer_keywords: ["ListView_SetTextColor","ListView_SetTextColor macro [Windows Controls]","_win32_ListView_SetTextColor","_win32_ListView_SetTextColor_cpp","commctrl/ListView_SetTextColor","controls.ListView_SetTextColor","controls._win32_ListView_SetTextColor"]
old-location: controls\ListView_SetTextColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settextcolor.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetTextColor, ListView_SetTextColor macro [Windows Controls], _win32_ListView_SetTextColor, _win32_ListView_SetTextColor_cpp, commctrl/ListView_SetTextColor, controls.ListView_SetTextColor, controls._win32_ListView_SetTextColor
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
 - ListView_SetTextColor
 - commctrl/ListView_SetTextColor
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
 - ListView_SetTextColor
---

# ListView_SetTextColor macro

## -syntax

```cpp
BOOL ListView_SetTextColor(
   HWND     hwnd,
   COLORREF clrText
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sets the text color of a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-settextcolor">LVM_SETTEXTCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param clrText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The new text color.
