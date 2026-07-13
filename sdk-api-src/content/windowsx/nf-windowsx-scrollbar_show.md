---
UID: NF:windowsx.ScrollBar_Show
title: ScrollBar_Show macro (windowsx.h)
description: Shows or hides a scroll bar control.
helpviewer_keywords: ["ScrollBar_Show","ScrollBar_Show macro [Windows Controls]","_win32_ScrollBar_Show","_win32_ScrollBar_Show_cpp","controls.ScrollBar_Show","controls._win32_ScrollBar_Show","windowsx/ScrollBar_Show"]
old-location: controls\ScrollBar_Show.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_show.htm
ms.date: 10/21/2024
ms.keywords: ScrollBar_Show, ScrollBar_Show macro [Windows Controls], _win32_ScrollBar_Show, _win32_ScrollBar_Show_cpp, controls.ScrollBar_Show, controls._win32_ScrollBar_Show, windowsx/ScrollBar_Show
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
 - ScrollBar_Show
 - windowsx/ScrollBar_Show
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
 - ScrollBar_Show
---

# ScrollBar_Show macro

## -syntax

```cpp
BOOL ScrollBar_Show(
   HWND hwndCtl,
   BOOL fShow
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

<b>TRUE</b> if the window was previously visible, or <b>FALSE</b> if it was previously hidden.


## -description

Shows or hides a scroll bar control.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param fShow

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to show the control, or <b>FALSE</b> to hide it.
