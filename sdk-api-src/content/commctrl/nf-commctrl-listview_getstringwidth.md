---
UID: NF:commctrl.ListView_GetStringWidth
title: ListView_GetStringWidth macro (commctrl.h)
description: Determines the width of a specified string using the specified list-view control's current font. You can use this macro or send the LVM_GETSTRINGWIDTH message explicitly.
helpviewer_keywords: ["ListView_GetStringWidth","ListView_GetStringWidth macro [Windows Controls]","_win32_ListView_GetStringWidth","_win32_ListView_GetStringWidth_cpp","commctrl/ListView_GetStringWidth","controls.ListView_GetStringWidth","controls._win32_ListView_GetStringWidth"]
old-location: controls\ListView_GetStringWidth.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getstringwidth.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetStringWidth, ListView_GetStringWidth macro [Windows Controls], _win32_ListView_GetStringWidth, _win32_ListView_GetStringWidth_cpp, commctrl/ListView_GetStringWidth, controls.ListView_GetStringWidth, controls._win32_ListView_GetStringWidth
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
 - ListView_GetStringWidth
 - commctrl/ListView_GetStringWidth
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
 - ListView_GetStringWidth
---

# ListView_GetStringWidth macro

## -syntax

```cpp
int ListView_GetStringWidth(
   HWND   hwndLV,
   LPCSTR psz
);
```

## -returns

Type: **int**

Returns the string width if successful, or zero otherwise.


## -description

Determines the width of a specified string using the specified list-view control's current font. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getstringwidth">LVM_GETSTRINGWIDTH</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param psz

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A pointer to a null-terminated string.

## -remarks

The <b>ListView_GetStringWidth</b> macro returns the exact width, in pixels, of the specified string. If you use the returned string width as the column width in a call to the <a href="/windows/desktop/api/commctrl/nf-commctrl-listview_setcolumnwidth">ListView_SetColumnWidth</a> macro, the string will be truncated. To retrieve the column width that can contain the string without truncating it, you must add padding to the returned string width.
