---
UID: NF:commctrl.MonthCal_SetMonthDelta
title: MonthCal_SetMonthDelta macro (commctrl.h)
description: Sets the scroll rate for a month calendar control. The scroll rate is the number of months that the control moves its display when the user clicks a scroll button. You can use this macro or send the MCM_SETMONTHDELTA message explicitly.
helpviewer_keywords: ["MonthCal_SetMonthDelta","MonthCal_SetMonthDelta macro [Windows Controls]","_win32_MonthCal_SetMonthDelta","_win32_MonthCal_SetMonthDelta_cpp","commctrl/MonthCal_SetMonthDelta","controls.MonthCal_SetMonthDelta","controls._win32_MonthCal_SetMonthDelta"]
old-location: controls\MonthCal_SetMonthDelta.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setmonthdelta.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_SetMonthDelta, MonthCal_SetMonthDelta macro [Windows Controls], _win32_MonthCal_SetMonthDelta, _win32_MonthCal_SetMonthDelta_cpp, commctrl/MonthCal_SetMonthDelta, controls.MonthCal_SetMonthDelta, controls._win32_MonthCal_SetMonthDelta
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
 - MonthCal_SetMonthDelta
 - commctrl/MonthCal_SetMonthDelta
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
 - MonthCal_SetMonthDelta
---

# MonthCal_SetMonthDelta macro

## -syntax

```cpp
INT MonthCal_SetMonthDelta(
   HWND hmc,
   INT  n
);
```

## -returns

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

Returns an INT value that represents the previous scroll rate. If the scroll rate was not previously set, the return value is zero.


## -description

Sets the scroll rate for a month calendar control. The scroll rate is the number of months that the control moves its display when the user clicks a scroll button. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-setmonthdelta">MCM_SETMONTHDELTA</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param n

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Value representing the number of months to be set as the control's scroll rate. If this value is zero, the month delta is reset to the default, which is the number of months displayed in the control.

## -remarks

The PAGE UP and PAGE DOWN keys, VK_PRIOR and VK_NEXT, change the selected month by one, regardless of the number of months displayed or the value set by <a href="/windows/desktop/Controls/mcm-setmonthdelta">MCM_SETMONTHDELTA</a>.
