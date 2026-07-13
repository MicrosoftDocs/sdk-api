---
UID: NF:commctrl.Header_SetFocusedItem
title: Header_SetFocusedItem macro (commctrl.h)
description: Sets the focus to a specified item in a header control. Use this macro or send the HDM_SETFOCUSEDITEM message explicitly.
helpviewer_keywords: ["Header_SetFocusedItem","Header_SetFocusedItem macro [Windows Controls]","_shell_Header_SetFocusedItem","_shell_Header_SetFocusedItem_cpp","commctrl/Header_SetFocusedItem","controls.Header_SetFocusedItem","controls._shell_Header_SetFocusedItem"]
old-location: controls\Header_SetFocusedItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setfocuseditem.htm
ms.date: 10/21/2024
ms.keywords: Header_SetFocusedItem, Header_SetFocusedItem macro [Windows Controls], _shell_Header_SetFocusedItem, _shell_Header_SetFocusedItem_cpp, commctrl/Header_SetFocusedItem, controls.Header_SetFocusedItem, controls._shell_Header_SetFocusedItem
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Header_SetFocusedItem
 - commctrl/Header_SetFocusedItem
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
 - Header_SetFocusedItem
---

# Header_SetFocusedItem macro

## -syntax

```cpp
BOOL Header_SetFocusedItem(
  [in] HWND hwnd,
  [in] int  iItem
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sets the focus to a specified item in a header control. Use this macro or send the <a href="/windows/desktop/Controls/hdm-setfocuseditem">HDM_SETFOCUSEDITEM</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control.

### -param iItem [in]

Type: <b>int</b>

The index of item.

## -see-also

<a href="/windows/desktop/Controls/header-controls">About Header Controls</a>
