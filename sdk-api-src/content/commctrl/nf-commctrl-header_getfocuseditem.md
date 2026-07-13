---
UID: NF:commctrl.Header_GetFocusedItem
title: Header_GetFocusedItem macro (commctrl.h)
description: Gets the item in a header control that has the focus. Use this macro or send the HDM_GETFOCUSEDITEM message explicitly.
helpviewer_keywords: ["Header_GetFocusedItem","Header_GetFocusedItem macro [Windows Controls]","_shell_Header_GetFocusedItem","_shell_Header_GetFocusedItem_cpp","commctrl/Header_GetFocusedItem","controls.Header_GetFocusedItem","controls._shell_Header_GetFocusedItem"]
old-location: controls\Header_GetFocusedItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getfocuseditem.htm
ms.date: 10/21/2024
ms.keywords: Header_GetFocusedItem, Header_GetFocusedItem macro [Windows Controls], _shell_Header_GetFocusedItem, _shell_Header_GetFocusedItem_cpp, commctrl/Header_GetFocusedItem, controls.Header_GetFocusedItem, controls._shell_Header_GetFocusedItem
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
 - Header_GetFocusedItem
 - commctrl/Header_GetFocusedItem
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
 - Header_GetFocusedItem
---

# Header_GetFocusedItem macro

## -syntax

```cpp
int Header_GetFocusedItem(
   HWND hwnd
);
```

## -returns

Type: **int**

Returns the index of the item in focus.


## -description

Gets the item in a header control that has the focus. Use this macro or send the <a href="/windows/desktop/Controls/hdm-getfocuseditem">HDM_GETFOCUSEDITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control.

## -see-also

<a href="/windows/desktop/Controls/header-controls">About Header Controls</a>
