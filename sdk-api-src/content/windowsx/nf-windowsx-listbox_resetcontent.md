---
UID: NF:windowsx.ListBox_ResetContent
title: ListBox_ResetContent macro (windowsx.h)
description: Removes all items from a list box. You can use this macro or send the LB_RESETCONTENT message explicitly.
helpviewer_keywords: ["ListBox_ResetContent","ListBox_ResetContent macro [Windows Controls]","_win32_ListBox_ResetContent","_win32_ListBox_ResetContent_cpp","controls.ListBox_ResetContent","controls._win32_ListBox_ResetContent","windowsx/ListBox_ResetContent"]
old-location: controls\ListBox_ResetContent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_resetcontent.htm
ms.date: 10/21/2024
ms.keywords: ListBox_ResetContent, ListBox_ResetContent macro [Windows Controls], _win32_ListBox_ResetContent, _win32_ListBox_ResetContent_cpp, controls.ListBox_ResetContent, controls._win32_ListBox_ResetContent, windowsx/ListBox_ResetContent
req.header: windowsx.h
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
 - ListBox_ResetContent
 - windowsx/ListBox_ResetContent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ListBox_ResetContent
---

# ListBox_ResetContent macro

## -syntax

```cpp
BOOL ListBox_ResetContent(
   HWND hwndCtl
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

The return value is not meaningful.


## -description

Removes all items from a list box.  You can use this macro or send the <a href="/windows/desktop/Controls/lb-resetcontent">LB_RESETCONTENT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.
