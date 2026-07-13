---
UID: NF:commctrl.Header_DeleteItem
title: Header_DeleteItem macro (commctrl.h)
description: Deletes an item from a header control. You can use this macro or send the HDM_DELETEITEM message explicitly.
helpviewer_keywords: ["Header_DeleteItem","Header_DeleteItem macro [Windows Controls]","_win32_Header_DeleteItem","_win32_Header_DeleteItem_cpp","commctrl/Header_DeleteItem","controls.Header_DeleteItem","controls._win32_Header_DeleteItem"]
old-location: controls\Header_DeleteItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_deleteitem.htm
ms.date: 10/21/2024
ms.keywords: Header_DeleteItem, Header_DeleteItem macro [Windows Controls], _win32_Header_DeleteItem, _win32_Header_DeleteItem_cpp, commctrl/Header_DeleteItem, controls.Header_DeleteItem, controls._win32_Header_DeleteItem
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
 - Header_DeleteItem
 - commctrl/Header_DeleteItem
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
 - Header_DeleteItem
---

# Header_DeleteItem macro

## -syntax

```cpp
BOOL Header_DeleteItem(
   HWND hwndHD,
   int  i
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Deletes an item from a header control. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-deleteitem">HDM_DELETEITEM</a> message explicitly.

## -parameters

### -param hwndHD

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control.

### -param i

Type: <b>int</b>

An index of the item to delete.

## -remarks

The <b>Header_DeleteItem</b> macro is defined as follows. 


``` syntax
#define Header_DeleteItem(hwndHD, i)     \

      (BOOL)SendMessage((hwndHD), HDM_DELETEITEM, (WPARAM)(int)(i), 0L)
```

