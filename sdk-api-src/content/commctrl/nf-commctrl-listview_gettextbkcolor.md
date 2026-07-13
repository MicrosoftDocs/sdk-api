---
UID: NF:commctrl.ListView_GetTextBkColor
title: ListView_GetTextBkColor macro (commctrl.h)
description: Gets the text background color of a list-view control. You can use this macro or send the LVM_GETTEXTBKCOLOR message explicitly.
helpviewer_keywords: ["ListView_GetTextBkColor","ListView_GetTextBkColor macro [Windows Controls]","_win32_ListView_GetTextBkColor","_win32_ListView_GetTextBkColor_cpp","commctrl/ListView_GetTextBkColor","controls.ListView_GetTextBkColor","controls._win32_ListView_GetTextBkColor"]
old-location: controls\ListView_GetTextBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gettextbkcolor.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetTextBkColor, ListView_GetTextBkColor macro [Windows Controls], _win32_ListView_GetTextBkColor, _win32_ListView_GetTextBkColor_cpp, commctrl/ListView_GetTextBkColor, controls.ListView_GetTextBkColor, controls._win32_ListView_GetTextBkColor
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
 - ListView_GetTextBkColor
 - commctrl/ListView_GetTextBkColor
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
 - ListView_GetTextBkColor
---

# ListView_GetTextBkColor macro

## -syntax

```cpp
COLORREF ListView_GetTextBkColor(
   HWND hwnd
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns the background color of the text.


## -description

Gets the text background color of a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-gettextbkcolor">LVM_GETTEXTBKCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.
