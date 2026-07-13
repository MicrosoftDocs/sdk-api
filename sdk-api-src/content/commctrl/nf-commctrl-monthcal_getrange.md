---
UID: NF:commctrl.MonthCal_GetRange
title: MonthCal_GetRange macro (commctrl.h)
description: Retrieves the minimum and maximum allowable dates set for a month calendar control. You can use this macro or send the MCM_GETRANGE message explicitly.
helpviewer_keywords: ["MonthCal_GetRange","MonthCal_GetRange macro [Windows Controls]","_win32_MonthCal_GetRange","_win32_MonthCal_GetRange_cpp","commctrl/MonthCal_GetRange","controls.MonthCal_GetRange","controls._win32_MonthCal_GetRange"]
old-location: controls\MonthCal_GetRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getrange.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetRange, MonthCal_GetRange macro [Windows Controls], _win32_MonthCal_GetRange, _win32_MonthCal_GetRange_cpp, commctrl/MonthCal_GetRange, controls.MonthCal_GetRange, controls._win32_MonthCal_GetRange
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
 - MonthCal_GetRange
 - commctrl/MonthCal_GetRange
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
 - MonthCal_GetRange
---

# MonthCal_GetRange macro

## -syntax

```cpp
DWORD MonthCal_GetRange(
   HWND         hmc,
   LPSYSTEMTIME rgst
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns a <b>DWORD</b> value that can be zero (no limits are set) or a combination of the following values that specify limit information:

| Return code | Description |
|---|---|
| GDTR_MAX | There is a maximum limit set for the control; rgst[0] is valid and contains the applicable date information.  |
| GDTR_MIN | There is a minimum limit set for the control; rgst[1] is valid and contains the applicable date information.  |


## -description

Retrieves the minimum and maximum allowable dates set for a month calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getrange">MCM_GETRANGE</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param rgst

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structures that will receive the date limit information. The minimum limit is set in <i>rgst</i>[0], and <i>rgst</i>[1] receives the maximum limit. If either element is set to all zeros, then no corresponding limit is set for the month calendar control. The time members of these structures will not be modified. This parameter must be a valid address and cannot be <b>NULL</b>.
