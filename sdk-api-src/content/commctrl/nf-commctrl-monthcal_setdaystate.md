---
UID: NF:commctrl.MonthCal_SetDayState
title: MonthCal_SetDayState macro (commctrl.h)
description: Sets the day states for all months that are currently visible within a month calendar control. You can use this macro or send the MCM_SETDAYSTATE message explicitly.helpviewer_keywords: ["MonthCal_SetDayState","MonthCal_SetDayState macro [Windows Controls]","_win32_MonthCal_SetDayState","_win32_MonthCal_SetDayState_cpp","commctrl/MonthCal_SetDayState","controls.MonthCal_SetDayState","controls._win32_MonthCal_SetDayState"]
old-location: controls\MonthCal_SetDayState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setdaystate.htm
ms.date: 12/05/2018
ms.keywords: MonthCal_SetDayState, MonthCal_SetDayState macro [Windows Controls], _win32_MonthCal_SetDayState, _win32_MonthCal_SetDayState_cpp, commctrl/MonthCal_SetDayState, controls.MonthCal_SetDayState, controls._win32_MonthCal_SetDayState
f1_keywords:
- commctrl/MonthCal_SetDayState
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- MonthCal_SetDayState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MonthCal_SetDayState macro


## -description


Sets the day states for all months that are currently visible within a month calendar control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcm-setdaystate">MCM_SETDAYSTATE</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control. 


### -param cbds

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">INT</a></b>

Value of type <b>int</b> indicating how many elements are in the array that <i>lpDayStateArray</i> points to. 


### -param rgds

Type: <b>LPMONTHDAYSTATE</b>

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/Controls/monthdaystate">MONTHDAYSTATE</a> values that define how the month calendar control will draw each day in its display. 


## -remarks



An application can explicitly set day state information by using this macro, but the state will not persist when a different part of the calendar is scrolled into view. Day state information is usually set in response to the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcn-getdaystate">MCN_GETDAYSTATE</a> notification code, which is sent whenever the control needs to be refreshed.

The array at 
				<i>lpDayStateArray</i> must contain as many elements as the value returned by the following macro: 

<code>MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);</code>

The preceding macro returns the total number of months that are in complete or partial view within the month calendar's display. 

Keep in mind that the array at 
				<i>lpDayStateArray</i> must contain <a href="https://docs.microsoft.com/windows/desktop/Controls/monthdaystate">MONTHDAYSTATE</a> values that correspond with all months currently in the control's display, in chronological order. This includes the two months that may be  partially displayed before the first month and after the last month.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/using-month-calendar-controls">Using Month Calendar Controls</a>
 

 

