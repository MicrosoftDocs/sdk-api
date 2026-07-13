---
UID: NF:commctrl.Header_GetOverflowRect
title: Header_GetOverflowRect macro (commctrl.h)
description: Gets the coordinates of the drop-down overflow area for a specified header control. The header control must be of type HDF_SPLITBUTTON. Use this macro or send the HDM_GETOVERFLOWRECT message explicitly.
helpviewer_keywords: ["Header_GetOverflowRect","Header_GetOverflowRect macro [Windows Controls]","_shell_Header_GetOverflowRect","_shell_Header_GetOverflowRect_cpp","commctrl/Header_GetOverflowRect","controls.Header_GetOverflowRect","controls._shell_Header_GetOverflowRect"]
old-location: controls\Header_GetOverflowRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getoverflowrect.htm
ms.date: 10/21/2024
ms.keywords: Header_GetOverflowRect, Header_GetOverflowRect macro [Windows Controls], _shell_Header_GetOverflowRect, _shell_Header_GetOverflowRect_cpp, commctrl/Header_GetOverflowRect, controls.Header_GetOverflowRect, controls._shell_Header_GetOverflowRect
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
 - Header_GetOverflowRect
 - commctrl/Header_GetOverflowRect
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
 - Header_GetOverflowRect
---

# Header_GetOverflowRect macro

## -syntax

```cpp
BOOL Header_GetOverflowRect(
  [in]      HWND   hwnd,
  [in, out] LPRECT lprc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.


## -description

Gets the coordinates of the drop-down overflow area for a specified header control. The header control must be of type <b>HDF_SPLITBUTTON</b>. Use this macro or send the <a href="/windows/desktop/Controls/hdm-getoverflowrect">HDM_GETOVERFLOWRECT</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control.

### -param lprc [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure to receive the bounding rectangle information.The message sender is responsible for allocating this structure. The coordinates returned in the <b>RECT</b> structure are expressed as screen coordinates.
