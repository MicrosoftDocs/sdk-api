---
UID: NF:commctrl.Header_GetItemRect
title: Header_GetItemRect macro (commctrl.h)
description: Gets the bounding rectangle for a given item in a header control. You can use this macro or send the HDM_GETITEMRECT message explicitly.
helpviewer_keywords: ["Header_GetItemRect","Header_GetItemRect macro [Windows Controls]","_win32_Header_GetItemRect","_win32_Header_GetItemRect_cpp","commctrl/Header_GetItemRect","controls.Header_GetItemRect","controls._win32_Header_GetItemRect"]
old-location: controls\Header_GetItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getitemrect.htm
ms.date: 10/21/2024
ms.keywords: Header_GetItemRect, Header_GetItemRect macro [Windows Controls], _win32_Header_GetItemRect, _win32_Header_GetItemRect_cpp, commctrl/Header_GetItemRect, controls.Header_GetItemRect, controls._win32_Header_GetItemRect
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
 - Header_GetItemRect
 - commctrl/Header_GetItemRect
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
 - Header_GetItemRect
---

# Header_GetItemRect macro

## -syntax

```cpp
BOOL Header_GetItemRect(
   HWND   hwnd,
   int    iItem,
   LPRECT lprc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Gets the bounding rectangle for a given item in a header control. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-getitemrect">HDM_GETITEMRECT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control.

### -param iItem

Type: <b>int</b>

The zero-based index of the header control item for which to retrieve the bounding rectangle.

### -param lprc

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the bounding rectangle information.
