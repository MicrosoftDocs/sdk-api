---
UID: NF:commctrl.Header_SetBitmapMargin
title: Header_SetBitmapMargin macro (commctrl.h)
description: Sets the width of the margin for a bitmap in an existing header control. You can use this macro or send the HDM_SETBITMAPMARGIN message explicitly.
helpviewer_keywords: ["Header_SetBitmapMargin","Header_SetBitmapMargin macro [Windows Controls]","_win32_Header_SetBitmapMargin","_win32_Header_SetBitmapMargin_cpp","commctrl/Header_SetBitmapMargin","controls.Header_SetBitmapMargin","controls._win32_Header_SetBitmapMargin"]
old-location: controls\Header_SetBitmapMargin.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setbitmapmargin.htm
ms.date: 10/21/2024
ms.keywords: Header_SetBitmapMargin, Header_SetBitmapMargin macro [Windows Controls], _win32_Header_SetBitmapMargin, _win32_Header_SetBitmapMargin_cpp, commctrl/Header_SetBitmapMargin, controls.Header_SetBitmapMargin, controls._win32_Header_SetBitmapMargin
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
 - Header_SetBitmapMargin
 - commctrl/Header_SetBitmapMargin
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
 - Header_SetBitmapMargin
---

# Header_SetBitmapMargin macro

## -syntax

```cpp
int Header_SetBitmapMargin(
   HWND hwnd,
   int  iWidth
);
```

## -returns

Type: **int**

Returns width of the bitmap margin in pixels. If the bitmap margin was not previously specified, the default value of 3*<b>GetSystemMetrics</b> (<i>CX_EDGE</i>) is returned.

## -description

Sets the width of the margin for a bitmap in an existing header control. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-setbitmapmargin">HDM_SETBITMAPMARGIN</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control.

### -param iWidth

Type: <b>int</b>

The width, specified in pixels, of the margin that surrounds a bitmap within an existing header control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-header_getbitmapmargin">Header_GetBitmapMargin</a>
