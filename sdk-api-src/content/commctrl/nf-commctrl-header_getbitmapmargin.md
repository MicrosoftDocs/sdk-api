---
UID: NF:commctrl.Header_GetBitmapMargin
title: Header_GetBitmapMargin macro (commctrl.h)
description: Gets the width of the margin (in pixels) of a bitmap in an existing header control. You can use this macro or send the HDM_GETBITMAPMARGIN message explicitly.
helpviewer_keywords: ["Header_GetBitmapMargin","Header_GetBitmapMargin macro [Windows Controls]","_win32_Header_GetBitmapMargin","_win32_Header_GetBitmapMargin_cpp","commctrl/Header_GetBitmapMargin","controls.Header_GetBitmapMargin","controls._win32_Header_GetBitmapMargin"]
old-location: controls\Header_GetBitmapMargin.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getbitmapmargin.htm
ms.date: 10/21/2024
ms.keywords: Header_GetBitmapMargin, Header_GetBitmapMargin macro [Windows Controls], _win32_Header_GetBitmapMargin, _win32_Header_GetBitmapMargin_cpp, commctrl/Header_GetBitmapMargin, controls.Header_GetBitmapMargin, controls._win32_Header_GetBitmapMargin
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
 - Header_GetBitmapMargin
 - commctrl/Header_GetBitmapMargin
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
 - Header_GetBitmapMargin
---

# Header_GetBitmapMargin macro

## -syntax

```cpp
int Header_GetBitmapMargin(
   HWND hwnd
);
```

## -returns

Type: **int**

Returns the width of the bitmap margin in pixels. If the bitmap margin was not previously specified, the default value of 3*<b>GetSystemMetrics</b> (<i>CX_EDGE</i>) is returned.

## -description

Gets the width of the margin (in pixels) of a bitmap in an existing header control. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-getbitmapmargin">HDM_GETBITMAPMARGIN</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-header_setbitmapmargin">Header_SetBitmapMargin</a>
