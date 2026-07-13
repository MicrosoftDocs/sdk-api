---
UID: NF:commctrl.MonthCal_GetMonthDelta
title: MonthCal_GetMonthDelta macro (commctrl.h)
description: Retrieves the scroll rate for a month calendar control. The scroll rate is the number of months that the control moves its display when the user clicks a scroll button. You can use this macro or send the MCM_GETMONTHDELTA message explicitly.
helpviewer_keywords: ["MonthCal_GetMonthDelta","MonthCal_GetMonthDelta macro [Windows Controls]","_win32_MonthCal_GetMonthDelta","_win32_MonthCal_GetMonthDelta_cpp","commctrl/MonthCal_GetMonthDelta","controls.MonthCal_GetMonthDelta","controls._win32_MonthCal_GetMonthDelta"]
old-location: controls\MonthCal_GetMonthDelta.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getmonthdelta.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetMonthDelta, MonthCal_GetMonthDelta macro [Windows Controls], _win32_MonthCal_GetMonthDelta, _win32_MonthCal_GetMonthDelta_cpp, commctrl/MonthCal_GetMonthDelta, controls.MonthCal_GetMonthDelta, controls._win32_MonthCal_GetMonthDelta
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
 - MonthCal_GetMonthDelta
 - commctrl/MonthCal_GetMonthDelta
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
 - MonthCal_GetMonthDelta
---

# MonthCal_GetMonthDelta macro

## -syntax

```cpp
INT MonthCal_GetMonthDelta(
   HWND hmc
);
```

## -returns

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

If the month delta was previously set using the <b>MonthCal_SetMonthDelta</b> macro, returns an INT value that represents the month calendar's current scroll rate. If the month delta was not previously set using the <b>MonthCal_SetMonthDelta</b> macro, or the month delta was reset to the default, returns an INT value that represents the current number of months visible.


## -description

Retrieves the scroll rate for a month calendar control. The scroll rate is the number of months that the control moves its display when the user clicks a scroll button. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getmonthdelta">MCM_GETMONTHDELTA</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.
