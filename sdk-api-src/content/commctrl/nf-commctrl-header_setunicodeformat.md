---
UID: NF:commctrl.Header_SetUnicodeFormat
title: Header_SetUnicodeFormat macro (commctrl.h)
description: Sets the UNICODE character format flag for the control.
helpviewer_keywords: ["Header_SetUnicodeFormat","Header_SetUnicodeFormat macro [Windows Controls]","_win32_Header_SetUnicodeFormat","_win32_Header_SetUnicodeFormat_cpp","commctrl/Header_SetUnicodeFormat","controls.Header_SetUnicodeFormat","controls._win32_Header_SetUnicodeFormat"]
old-location: controls\Header_SetUnicodeFormat.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setunicodeformat.htm
ms.date: 10/21/2024
ms.keywords: Header_SetUnicodeFormat, Header_SetUnicodeFormat macro [Windows Controls], _win32_Header_SetUnicodeFormat, _win32_Header_SetUnicodeFormat_cpp, commctrl/Header_SetUnicodeFormat, controls.Header_SetUnicodeFormat, controls._win32_Header_SetUnicodeFormat
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
 - Header_SetUnicodeFormat
 - commctrl/Header_SetUnicodeFormat
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
 - Header_SetUnicodeFormat
---

# Header_SetUnicodeFormat macro

## -syntax

```cpp
BOOL Header_SetUnicodeFormat(
   HWND hwnd,
   BOOL fUnicode
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns the previous Unicode format flag for the control.


## -description

Sets the UNICODE character format flag for the control. This message allows you to change the character set used by the control at run time rather than having to re-create the control. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-setunicodeformat">HDM_SETUNICODEFORMAT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param fUnicode

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Determines the character set that is used by the control. If this value is nonzero, the control will use Unicode characters. If this value is zero, the control will use ANSI characters.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-header_getunicodeformat">Header_GetUnicodeFormat</a>
