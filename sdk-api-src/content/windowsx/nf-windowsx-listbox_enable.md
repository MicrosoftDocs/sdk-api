---
UID: NF:windowsx.ListBox_Enable
title: ListBox_Enable macro (windowsx.h)
description: Enables or disables a list box control.
helpviewer_keywords: ["ListBox_Enable","ListBox_Enable macro [Windows Controls]","_win32_ListBox_Enable","_win32_ListBox_Enable_cpp","controls.ListBox_Enable","controls._win32_ListBox_Enable","windowsx/ListBox_Enable"]
old-location: controls\ListBox_Enable.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_enable.htm
ms.date: 10/21/2024
ms.keywords: ListBox_Enable, ListBox_Enable macro [Windows Controls], _win32_ListBox_Enable, _win32_ListBox_Enable_cpp, controls.ListBox_Enable, controls._win32_ListBox_Enable, windowsx/ListBox_Enable
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
 - ListBox_Enable
 - windowsx/ListBox_Enable
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
 - ListBox_Enable
---

# ListBox_Enable macro

## -syntax

```cpp
BOOL ListBox_Enable(
   HWND hwndCtl,
   BOOL fEnable
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

<b>TRUE</b> if the window was previously disabled, or <b>FALSE</b> if it was previously enabled.


## -description

Enables or disables a list box control.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param fEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to enable the control, or <b>FALSE</b> to disable it.
