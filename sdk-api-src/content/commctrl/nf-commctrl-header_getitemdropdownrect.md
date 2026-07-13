---
UID: NF:commctrl.Header_GetItemDropDownRect
title: Header_GetItemDropDownRect macro (commctrl.h)
description: Gets the coordinates of the drop-down button for a specified item in a header control. The header control must be of type HDF_SPLITBUTTON. Use this macro or send the HDM_GETITEMDROPDOWNRECT message explicitly.
helpviewer_keywords: ["Header_GetItemDropDownRect","Header_GetItemDropDownRect macro [Windows Controls]","_shell_Header_GetItemDropDownRect","_shell_Header_GetItemDropDownRect_cpp","commctrl/Header_GetItemDropDownRect","controls.Header_GetItemDropDownRect","controls._shell_Header_GetItemDropDownRect"]
old-location: controls\Header_GetItemDropDownRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getitemdropdownrect.htm
ms.date: 10/21/2024
ms.keywords: Header_GetItemDropDownRect, Header_GetItemDropDownRect macro [Windows Controls], _shell_Header_GetItemDropDownRect, _shell_Header_GetItemDropDownRect_cpp, commctrl/Header_GetItemDropDownRect, controls.Header_GetItemDropDownRect, controls._shell_Header_GetItemDropDownRect
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
 - Header_GetItemDropDownRect
 - commctrl/Header_GetItemDropDownRect
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
 - Header_GetItemDropDownRect
---

# Header_GetItemDropDownRect macro

## -syntax

```cpp
BOOL Header_GetItemDropDownRect(
  [in]      HWND   hwnd,
  [in]      int    iItem,
  [in, out] LPRECT lprc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>.


## -description

Gets the coordinates of the drop-down button for a specified item in a header control. The header control must be of type <b>HDF_SPLITBUTTON</b>. Use this macro or send the <a href="/windows/desktop/Controls/hdm-getitemdropdownrect">HDM_GETITEMDROPDOWNRECT</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control.

### -param iItem [in]

Type: <b>int</b>

The zero-based index of the header control item for which to retrieve the bounding rectangle.

### -param lprc [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure to receive the bounding rectangle information. The message sender is responsible for allocating this structure. The coordinates returned in the <b>RECT</b> structure are expressed as screen coordinates.
