---
UID: NF:commctrl.Header_GetItem
title: Header_GetItem macro (commctrl.h)
description: Gets information about an item in a header control. You can use this macro or send the HDM_GETITEM message explicitly.
helpviewer_keywords: ["Header_GetItem","Header_GetItem macro [Windows Controls]","_win32_Header_GetItem","_win32_Header_GetItem_cpp","commctrl/Header_GetItem","controls.Header_GetItem","controls._win32_Header_GetItem"]
old-location: controls\Header_GetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getitem.htm
ms.date: 10/21/2024
ms.keywords: Header_GetItem, Header_GetItem macro [Windows Controls], _win32_Header_GetItem, _win32_Header_GetItem_cpp, commctrl/Header_GetItem, controls.Header_GetItem, controls._win32_Header_GetItem
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
 - Header_GetItem
 - commctrl/Header_GetItem
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
 - Header_GetItem
---

# Header_GetItem macro

## -syntax

```cpp
BOOL Header_GetItem(
   HWND     hwndHD,
   int      i,
   LPHDITEM phdi
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Gets information about an item in a header control. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-getitem">HDM_GETITEM</a> message explicitly.

## -parameters

### -param hwndHD

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control.

### -param i

Type: <b>int</b>

The index of the item for which information is to be retrieved.

### -param phdi

Type: <b>LPHDITEM</b>

A pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-hditema">HDITEM</a> structure. When the message is sent, the <b>mask</b> member indicates the type of information being requested. When the message returns, the other members receive the requested information. If the 
<b>mask</b> member specifies zero, the message returns <b>TRUE</b> but copies no information to the structure.

## -remarks

If the HDI_TEXT flag is set in the 
				<b>mask</b> member of the <a href="/windows/win32/api/commctrl/ns-commctrl-hditema">HDITEM</a> structure, the control may change the 
				<b>pszText</b> member of the structure to point to the new text instead of filling the buffer with the requested text. Applications should not assume that the text will always be placed in the requested buffer.

The <b>Header_GetItem</b> macro is defined as follows:


``` syntax
#define Header_GetItem(hwndHD, i, phdi)      \

    (BOOL)SendMessage((hwndHD), HDM_GETITEM,   \

    (WPARAM)(int)(i), (LPARAM)(LPHDITEM)(phdi))
```

