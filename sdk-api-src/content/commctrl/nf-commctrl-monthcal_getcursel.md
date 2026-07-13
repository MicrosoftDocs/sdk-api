---
UID: NF:commctrl.MonthCal_GetCurSel
title: MonthCal_GetCurSel macro (commctrl.h)
description: Retrieves the currently selected date. You can use this macro or send the MCM_GETCURSEL message explicitly.
helpviewer_keywords: ["MonthCal_GetCurSel","MonthCal_GetCurSel macro [Windows Controls]","_win32_MonthCal_GetCurSel","_win32_MonthCal_GetCurSel_cpp","commctrl/MonthCal_GetCurSel","controls.MonthCal_GetCurSel","controls._win32_MonthCal_GetCurSel"]
old-location: controls\MonthCal_GetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getcursel.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetCurSel, MonthCal_GetCurSel macro [Windows Controls], _win32_MonthCal_GetCurSel, _win32_MonthCal_GetCurSel_cpp, commctrl/MonthCal_GetCurSel, controls.MonthCal_GetCurSel, controls._win32_MonthCal_GetCurSel
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
 - MonthCal_GetCurSel
 - commctrl/MonthCal_GetCurSel
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
 - MonthCal_GetCurSel
---

# MonthCal_GetCurSel macro

## -syntax

```cpp
BOOL MonthCal_GetCurSel(
   HWND         hmc,
   LPSYSTEMTIME pst
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise. This macro will always fail when applied to month calendar controls that are set to the <b>MCS_MULTISELECT</b> style.


## -description

Retrieves the currently selected date. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getcursel">MCM_GETCURSEL</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param pst

Type: <b>LPSYSTEMTIME</b>

Pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that will receive the currently selected date information. This parameter must be a valid address and cannot be <b>NULL</b>.
