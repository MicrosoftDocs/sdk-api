---
UID: NF:windowsx.ScrollBar_Enable
title: ScrollBar_Enable macro (windowsx.h)
description: Enables or disables a scroll bar control.
helpviewer_keywords: ["ScrollBar_Enable","ScrollBar_Enable macro [Windows Controls]","_win32_ScrollBar_Enable","_win32_ScrollBar_Enable_cpp","controls.ScrollBar_Enable","controls._win32_ScrollBar_Enable","windowsx/ScrollBar_Enable"]
old-location: controls\ScrollBar_Enable.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_enable.htm
ms.date: 10/21/2024
ms.keywords: ScrollBar_Enable, ScrollBar_Enable macro [Windows Controls], _win32_ScrollBar_Enable, _win32_ScrollBar_Enable_cpp, controls.ScrollBar_Enable, controls._win32_ScrollBar_Enable, windowsx/ScrollBar_Enable
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
 - ScrollBar_Enable
 - windowsx/ScrollBar_Enable
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
 - ScrollBar_Enable
---

# ScrollBar_Enable macro

## -syntax

```cpp
BOOL ScrollBar_Enable(
   HWND hwndCtl,
   UINT flags
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If the arrows are enabled or disabled as specified, the return value is nonzero.


## -description

Enables or disables a scroll bar control.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that specify the arrows affected and whether they are enabled or disabled. See the <i>wArrows</i> parameter of <a href="/windows/desktop/api/winuser/nf-winuser-enablescrollbar">EnableScrollBar</a> for more information.

## -remarks

The macro expands to a call to <a href="/windows/desktop/api/winuser/nf-winuser-enablescrollbar">EnableScrollBar</a> with SB_CTL in the <i>wSBFlags</i> parameter.
