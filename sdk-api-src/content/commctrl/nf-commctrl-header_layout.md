---
UID: NF:commctrl.Header_Layout
title: Header_Layout macro (commctrl.h)
description: Retrieves the correct size and position of a header control within the parent window. You can use this macro or send the HDM_LAYOUT message explicitly.
helpviewer_keywords: ["Header_Layout","Header_Layout macro [Windows Controls]","_win32_Header_Layout","_win32_Header_Layout_cpp","commctrl/Header_Layout","controls.Header_Layout","controls._win32_Header_Layout"]
old-location: controls\Header_Layout.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_layout.htm
ms.date: 10/21/2024
ms.keywords: Header_Layout, Header_Layout macro [Windows Controls], _win32_Header_Layout, _win32_Header_Layout_cpp, commctrl/Header_Layout, controls.Header_Layout, controls._win32_Header_Layout
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
 - Header_Layout
 - commctrl/Header_Layout
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
 - Header_Layout
---

# Header_Layout macro

## -syntax

```cpp
BOOL Header_Layout(
  [in]  HWND       hwndHD,
  [out] LPHDLAYOUT playout
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Retrieves the correct size and position of a header control within the parent window. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-layout">HDM_LAYOUT</a> message explicitly.

## -parameters

### -param hwndHD [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control.

### -param playout [out]

Type: <b>LPHDLAYOUT</b>

A pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-hdlayout">HDLAYOUT</a> structure. The 
					<b>prc</b> member specifies the coordinates of a rectangle, and the 
					<b>pwpos</b> member receives the size and position for the header control within the rectangle.

## -remarks

The <b>Header_Layout</b> macro is defined as follows: 


``` syntax
#define Header_Layout(hwndHD, playout) \

    (BOOL)SendMessage((hwndHD), HDM_LAYOUT, 0, \

    (LPARAM)(LPHDLAYOUT)(playout))
```

