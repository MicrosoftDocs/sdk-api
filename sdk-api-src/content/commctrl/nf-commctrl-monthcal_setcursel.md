---
UID: NF:commctrl.MonthCal_SetCurSel
title: MonthCal_SetCurSel macro (commctrl.h)
description: Sets the currently selected date for a month calendar control. If the specified date is not in view, the control updates the display to bring it into view. You can use this macro or send the MCM_SETCURSEL message explicitly.
helpviewer_keywords: ["MonthCal_SetCurSel","MonthCal_SetCurSel macro [Windows Controls]","_win32_MonthCal_SetCurSel","_win32_MonthCal_SetCurSel_cpp","commctrl/MonthCal_SetCurSel","controls.MonthCal_SetCurSel","controls._win32_MonthCal_SetCurSel"]
old-location: controls\MonthCal_SetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcursel.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_SetCurSel, MonthCal_SetCurSel macro [Windows Controls], _win32_MonthCal_SetCurSel, _win32_MonthCal_SetCurSel_cpp, commctrl/MonthCal_SetCurSel, controls.MonthCal_SetCurSel, controls._win32_MonthCal_SetCurSel
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
 - MonthCal_SetCurSel
 - commctrl/MonthCal_SetCurSel
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
 - MonthCal_SetCurSel
---

# MonthCal_SetCurSel macro

## -syntax

```cpp
BOOL MonthCal_SetCurSel(
   HWND         hmc,
   LPSYSTEMTIME pst
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise. This macro will fail if applied to a month calendar control that uses the <b>MCS_MULTISELECT</b> style.


## -description

Sets the currently selected date for a month calendar control. If the specified date is not in view, the control updates the display to bring it into view. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-setcursel">MCM_SETCURSEL</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param pst

Type: <b>LPSYSTEMTIME</b>

Pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date to be set as the current selection. The time members of this structure are ignored.
