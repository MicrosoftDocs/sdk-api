---
UID: NF:windowsx.ScrollBar_SetRange
title: ScrollBar_SetRange macro (windowsx.h)
description: Sets the range of a scroll bar.
helpviewer_keywords: ["ScrollBar_SetRange","ScrollBar_SetRange macro [Windows Controls]","_win32_ScrollBar_SetRange","_win32_ScrollBar_SetRange_cpp","controls.ScrollBar_SetRange","controls._win32_ScrollBar_SetRange","windowsx/ScrollBar_SetRange"]
old-location: controls\ScrollBar_SetRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_setrange.htm
ms.date: 10/21/2024
ms.keywords: ScrollBar_SetRange, ScrollBar_SetRange macro [Windows Controls], _win32_ScrollBar_SetRange, _win32_ScrollBar_SetRange_cpp, controls.ScrollBar_SetRange, controls._win32_ScrollBar_SetRange, windowsx/ScrollBar_SetRange
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
 - ScrollBar_SetRange
 - windowsx/ScrollBar_SetRange
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
 - ScrollBar_SetRange
---

# ScrollBar_SetRange macro

## -syntax

```cpp
BOOL ScrollBar_SetRange(
   HWND hwndCtl,
   int  posMin,
   int  posMax,
   BOOL fRedraw
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

<b>TRUE</b> if the call succeeded; otherwise <b>FALSE</b>.


## -description

Sets the range of a scroll bar.
        
<div class="alert"><b>Note</b>  This macro expands to a call to the <a href="/windows/desktop/api/winuser/nf-winuser-setscrollrange">SetScrollRange</a> function, which is deprecated. New applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a> function.</div><div> </div>

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param posMin

Type: <b>int</b>

The minimum value of the scroll bar.

### -param posMax

Type: <b>int</b>

The maximum value of the scroll bar.

### -param fRedraw

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to redraw the control; otherwise <b>FALSE</b>.

## -remarks

For more information, see <a href="/windows/desktop/api/winuser/nf-winuser-setscrollrange">SetScrollRange</a>.
