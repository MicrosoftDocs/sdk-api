---
UID: NF:commctrl.Pager_SetScrollInfo
title: Pager_SetScrollInfo macro (commctrl.h)
description: Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line. You can use this macro or send the PGM_SETSETSCROLLINFO message explicitly.
helpviewer_keywords: ["Pager_SetScrollInfo","Pager_SetScrollInfo macro [Windows Controls]","_win32_Pager_SetScrollInfo","_win32_Pager_SetScrollInfo_cpp","commctrl/Pager_SetScrollInfo","controls.Pager_SetScrollInfo","controls._win32_Pager_SetScrollInfo"]
old-location: controls\Pager_SetScrollInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setscrollinfo.htm
ms.date: 10/21/2024
ms.keywords: Pager_SetScrollInfo, Pager_SetScrollInfo macro [Windows Controls], _win32_Pager_SetScrollInfo, _win32_Pager_SetScrollInfo_cpp, commctrl/Pager_SetScrollInfo, controls.Pager_SetScrollInfo, controls._win32_Pager_SetScrollInfo
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
 - Pager_SetScrollInfo
 - commctrl/Pager_SetScrollInfo
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
 - Pager_SetScrollInfo
---

# Pager_SetScrollInfo macro

## -syntax

```cpp
int Pager_SetScrollInfo(
   HWND hwnd,
   UINT cTimeOut,
   UINT cLinesPer,
   UINT cPixelsPerLine
);
```

## -returns

Type: **int**

The return value is not used.


## -description

<p class="CCE_Message">[Intended for internal use; not recommended for use in applications. This macro may not be supported in future versions of Windows.]

Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line. You can use this macro or send the <a href="/windows/desktop/Controls/pgm-setscrollinfo">PGM_SETSETSCROLLINFO</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control.

### -param cTimeOut

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The timeout value for the scroll, in milliseconds.

### -param cLinesPer

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of lines to scroll per timeout.

### -param cPixelsPerLine

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of pixels per line.

## -remarks

This <i>cTimeOut</i> parameter controls the rate at which the pager control generates scrolling events when the control has captured the mouse input and the left mouse button is pressed. Smaller values result in faster scrolling; larger values result in slower scrolling. The default value is one-eighth of the double-click time. For more information, see <a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime">GetDoubleClickTime</a>.

By default, with each scrolling event the pager control scrolls an amount equal to the entire width or height of the control, depending on whether the pager control has a horizontal or vertical orientation. The <i>cLinesPer</i> and <i>cPixelsPerLine</i> parameters are used to override the default scrolling amount. If nonzero values are provided, the scrolling amount is the product of the two values (<i>cLinesPer</i> * <i>cPixelsPerLine</i>).

## -see-also

<a href="/windows/desktop/Controls/pgm-setscrollinfo">PGM_SETSETSCROLLINFO</a>
