---
UID: NF:commctrl.TabCtrl_SetItemSize
title: TabCtrl_SetItemSize macro (commctrl.h)
description: Sets the width and height of tabs in a fixed-width or owner-drawn tab control. You can use this macro or send the TCM_SETITEMSIZE message explicitly.
helpviewer_keywords: ["TabCtrl_SetItemSize","TabCtrl_SetItemSize macro [Windows Controls]","_win32_TabCtrl_SetItemSize","_win32_TabCtrl_SetItemSize_cpp","commctrl/TabCtrl_SetItemSize","controls.TabCtrl_SetItemSize","controls._win32_TabCtrl_SetItemSize"]
old-location: controls\TabCtrl_SetItemSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setitemsize.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_SetItemSize, TabCtrl_SetItemSize macro [Windows Controls], _win32_TabCtrl_SetItemSize, _win32_TabCtrl_SetItemSize_cpp, commctrl/TabCtrl_SetItemSize, controls.TabCtrl_SetItemSize, controls._win32_TabCtrl_SetItemSize
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
 - TabCtrl_SetItemSize
 - commctrl/TabCtrl_SetItemSize
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
 - TabCtrl_SetItemSize
---

# TabCtrl_SetItemSize macro

## -syntax

```cpp
DWORD TabCtrl_SetItemSize(
   HWND hwnd,
   int  x,
   int  y
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the old width and height. The width is in the <b>LOWORD</b> of the return value, and the height is in the <b>HIWORD</b>.


## -description

Sets the width and height of tabs in a fixed-width or owner-drawn tab control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-setitemsize">TCM_SETITEMSIZE</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control.

### -param x

Type: <b>int</b>

New width, in pixels.

### -param y

Type: <b>int</b>

New height, in pixels.
