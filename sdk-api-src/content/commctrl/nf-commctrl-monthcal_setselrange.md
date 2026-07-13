---
UID: NF:commctrl.MonthCal_SetSelRange
title: MonthCal_SetSelRange macro (commctrl.h)
description: Sets the selection for a month calendar control to a given date range. You can use this macro or send the MCM_SETSELRANGE message explicitly.
helpviewer_keywords: ["MonthCal_SetSelRange","MonthCal_SetSelRange macro [Windows Controls]","_win32_MonthCal_SetSelRange","_win32_MonthCal_SetSelRange_cpp","commctrl/MonthCal_SetSelRange","controls.MonthCal_SetSelRange","controls._win32_MonthCal_SetSelRange"]
old-location: controls\MonthCal_SetSelRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setselrange.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_SetSelRange, MonthCal_SetSelRange macro [Windows Controls], _win32_MonthCal_SetSelRange, _win32_MonthCal_SetSelRange_cpp, commctrl/MonthCal_SetSelRange, controls.MonthCal_SetSelRange, controls._win32_MonthCal_SetSelRange
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
 - MonthCal_SetSelRange
 - commctrl/MonthCal_SetSelRange
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
 - MonthCal_SetSelRange
---

# MonthCal_SetSelRange macro

## -syntax

```cpp
BOOL MonthCal_SetSelRange(
   HWND         hmc,
   LPSYSTEMTIME rgst
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise. This macro will fail if applied to a month calendar control that does not use the <b>MCS_MULTISELECT</b> style.


## -description

Sets the selection for a month calendar control to a given date range. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-setselrange">MCM_SETSELRANGE</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param rgst

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structures that contain date information representing the selection limits. The first selected date must be specified in <i>rgst</i>[0], and the last selected date must be specified in <i>rgst</i>[1]. The time members of these structures are ignored.
