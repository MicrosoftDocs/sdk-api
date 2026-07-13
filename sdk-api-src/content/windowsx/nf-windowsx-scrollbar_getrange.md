---
UID: NF:windowsx.ScrollBar_GetRange
title: ScrollBar_GetRange macro (windowsx.h)
description: Gets the range of a scroll bar.
helpviewer_keywords: ["ScrollBar_GetRange","ScrollBar_GetRange macro [Windows Controls]","_win32_ScrollBar_GetRange","_win32_ScrollBar_GetRange_cpp","controls.ScrollBar_GetRange","controls._win32_ScrollBar_GetRange","windowsx/ScrollBar_GetRange"]
old-location: controls\ScrollBar_GetRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_getrange.htm
ms.date: 10/21/2024
ms.keywords: ScrollBar_GetRange, ScrollBar_GetRange macro [Windows Controls], _win32_ScrollBar_GetRange, _win32_ScrollBar_GetRange_cpp, controls.ScrollBar_GetRange, controls._win32_ScrollBar_GetRange, windowsx/ScrollBar_GetRange
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
 - ScrollBar_GetRange
 - windowsx/ScrollBar_GetRange
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
 - ScrollBar_GetRange
---

# ScrollBar_GetRange macro

## -syntax

```cpp
BOOL ScrollBar_GetRange(
   HWND hwndCtl,
   int  *lpposMin,
   int  *lpposMax
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

<b>TRUE</b> if the call succeeded; otherwise <b>FALSE</b>.


## -description

Gets the range of a scroll bar.
        
<div class="alert"><b>Note</b>  This macro expands to a call to the <a href="/windows/desktop/api/winuser/nf-winuser-getscrollrange">GetScrollRange</a> function, which is deprecated. New applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a> function.</div><div> </div>

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param lpposMin

Type: <b>int*</b>

Address of a variable that receives the minimum value of the scroll bar.

### -param lpposMax

Type: <b>int*</b>

Address of a variable that receives the maximum value of the scroll bar.

## -remarks

For more information, see <a href="/windows/desktop/api/winuser/nf-winuser-getscrollrange">GetScrollRange</a>.
