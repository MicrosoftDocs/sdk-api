---
UID: NF:commctrl.ListView_GetHotCursor
title: ListView_GetHotCursor macro (commctrl.h)
description: Gets the HCURSOR used when the pointer is over an item while hot tracking is enabled. You can use this macro or send the LVM_GETHOTCURSOR message explicitly.
helpviewer_keywords: ["ListView_GetHotCursor","ListView_GetHotCursor macro [Windows Controls]","_win32_ListView_GetHotCursor","_win32_ListView_GetHotCursor_cpp","commctrl/ListView_GetHotCursor","controls.ListView_GetHotCursor","controls._win32_ListView_GetHotCursor"]
old-location: controls\ListView_GetHotCursor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gethotcursor.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetHotCursor, ListView_GetHotCursor macro [Windows Controls], _win32_ListView_GetHotCursor, _win32_ListView_GetHotCursor_cpp, commctrl/ListView_GetHotCursor, controls.ListView_GetHotCursor, controls._win32_ListView_GetHotCursor
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
 - ListView_GetHotCursor
 - commctrl/ListView_GetHotCursor
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
 - ListView_GetHotCursor
---

# ListView_GetHotCursor macro

## -syntax

```cpp
HCURSOR ListView_GetHotCursor(
   HWND hwnd
);
```

## -returns

Type: **[HCURSOR](/windows/desktop/winprog/windows-data-types)**

Returns an HCURSOR value that is the handle to the cursor that the list-view control uses when hot tracking is enabled.


## -description

Gets the HCURSOR used when the pointer is over an item while hot tracking is enabled. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-gethotcursor">LVM_GETHOTCURSOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control.

## -remarks

A list-view control uses hot tracking and hover selection when the <a href="/windows/desktop/Controls/extended-list-view-styles">LVS_EX_TRACKSELECT</a> style is set.
