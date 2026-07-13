---
UID: NF:commctrl.TabCtrl_GetUnicodeFormat
title: TabCtrl_GetUnicodeFormat macro (commctrl.h)
description: Retrieves the UNICODE character format flag for the control. You can use this macro or send the TCM_GETUNICODEFORMAT message explicitly.
helpviewer_keywords: ["TabCtrl_GetUnicodeFormat","TabCtrl_GetUnicodeFormat macro [Windows Controls]","_win32_TabCtrl_GetUnicodeFormat","_win32_TabCtrl_GetUnicodeFormat_cpp","commctrl/TabCtrl_GetUnicodeFormat","controls.TabCtrl_GetUnicodeFormat","controls._win32_TabCtrl_GetUnicodeFormat"]
old-location: controls\TabCtrl_GetUnicodeFormat.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getunicodeformat.htm
ms.date: 10/21/2024
ms.keywords: TabCtrl_GetUnicodeFormat, TabCtrl_GetUnicodeFormat macro [Windows Controls], _win32_TabCtrl_GetUnicodeFormat, _win32_TabCtrl_GetUnicodeFormat_cpp, commctrl/TabCtrl_GetUnicodeFormat, controls.TabCtrl_GetUnicodeFormat, controls._win32_TabCtrl_GetUnicodeFormat
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
 - TabCtrl_GetUnicodeFormat
 - commctrl/TabCtrl_GetUnicodeFormat
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
 - TabCtrl_GetUnicodeFormat
---

# TabCtrl_GetUnicodeFormat macro

## -syntax

```cpp
BOOL TabCtrl_GetUnicodeFormat(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns the Unicode format flag for the control. If this value is nonzero, the control is using Unicode characters. If this value is zero, the control is using ANSI characters.


## -description

Retrieves the UNICODE character format flag for the control. You can use this macro or send the <a href="/windows/desktop/Controls/tcm-getunicodeformat">TCM_GETUNICODEFORMAT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-tabctrl_setunicodeformat">TabCtrl_SetUnicodeFormat</a>
