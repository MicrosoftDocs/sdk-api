---
UID: NF:commctrl.ListView_GetTextColor
title: ListView_GetTextColor macro (commctrl.h)
description: Gets the text color of a list-view control. You can use this macro or send the LVM_GETTEXTCOLOR message explicitly.
helpviewer_keywords: ["ListView_GetTextColor","ListView_GetTextColor macro [Windows Controls]","_win32_ListView_GetTextColor","_win32_ListView_GetTextColor_cpp","commctrl/ListView_GetTextColor","controls.ListView_GetTextColor","controls._win32_ListView_GetTextColor"]
old-location: controls\ListView_GetTextColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gettextcolor.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetTextColor, ListView_GetTextColor macro [Windows Controls], _win32_ListView_GetTextColor, _win32_ListView_GetTextColor_cpp, commctrl/ListView_GetTextColor, controls.ListView_GetTextColor, controls._win32_ListView_GetTextColor
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
 - ListView_GetTextColor
 - commctrl/ListView_GetTextColor
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
 - ListView_GetTextColor
---

# ListView_GetTextColor macro

## -syntax

```cpp
COLORREF ListView_GetTextColor(
   HWND hwnd
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns the text color.


## -description

Gets the text color of a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-gettextcolor">LVM_GETTEXTCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.
