---
UID: NF:commctrl.MonthCal_SetUnicodeFormat
title: MonthCal_SetUnicodeFormat macro (commctrl.h)
description: Sets the Unicode character format flag for the control. (MonthCal_SetUnicodeFormat)
helpviewer_keywords: ["MonthCal_SetUnicodeFormat","MonthCal_SetUnicodeFormat macro [Windows Controls]","_win32_MonthCal_SetUnicodeFormat","_win32_MonthCal_SetUnicodeFormat_cpp","commctrl/MonthCal_SetUnicodeFormat","controls.MonthCal_SetUnicodeFormat","controls._win32_MonthCal_SetUnicodeFormat"]
old-location: controls\MonthCal_SetUnicodeFormat.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setunicodeformat.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_SetUnicodeFormat, MonthCal_SetUnicodeFormat macro [Windows Controls], _win32_MonthCal_SetUnicodeFormat, _win32_MonthCal_SetUnicodeFormat_cpp, commctrl/MonthCal_SetUnicodeFormat, controls.MonthCal_SetUnicodeFormat, controls._win32_MonthCal_SetUnicodeFormat
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
 - MonthCal_SetUnicodeFormat
 - commctrl/MonthCal_SetUnicodeFormat
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
 - MonthCal_SetUnicodeFormat
---

# MonthCal_SetUnicodeFormat macro

## -syntax

```cpp
BOOL MonthCal_SetUnicodeFormat(
   HWND hwnd,
   BOOL fUnicode
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns the previous Unicode format flag for the control.


## -description

Sets the Unicode character format flag for the control. This message allows you to change the character set used by the control at run time rather than having to re-create the control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-setunicodeformat">MCM_SETUNICODEFORMAT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the control.

### -param fUnicode

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Determines the character set that is used by the control. If this value is nonzero, the control will use Unicode characters. If this value is zero, the control will use ANSI characters.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-monthcal_getunicodeformat">MonthCal_GetUnicodeFormat</a>
