---
UID: NF:commctrl.MonthCal_SetDayState
title: MonthCal_SetDayState macro
author: windows-sdk-content
description: Sets the day states for all months that are currently visible within a month calendar control. You can use this macro or send the MCM_SETDAYSTATE message explicitly.
old-location: controls\MonthCal_SetDayState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setdaystate.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MonthCal_SetDayState, MonthCal_SetDayState macro [Windows Controls], _win32_MonthCal_SetDayState, _win32_MonthCal_SetDayState_cpp, commctrl/MonthCal_SetDayState, controls.MonthCal_SetDayState, controls._win32_MonthCal_SetDayState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- MonthCal_SetDayState
: 
---

# MonthCal_SetDayState macro


## -description


Sets the day states for all months that are currently visible within a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761004(v=VS.85).aspx">MCM_SETDAYSTATE</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to a month calendar control. 


### -param cbds

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">INT</a></b>

Value of type <b>int</b> indicating how many elements are in the array that <i>lpDayStateArray</i> points to. 


### -param rgds

Type: <b>LPMONTHDAYSTATE</b>

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Bb760915(v=VS.85).aspx">MONTHDAYSTATE</a> values that define how the month calendar control will draw each day in its display. 


## -remarks



An application can explicitly set day state information by using this macro, but the state will not persist when a different part of the calendar is scrolled into view. Day state information is usually set in response to the <a href="https://msdn.microsoft.com/en-us/library/Bb760935(v=VS.85).aspx">MCN_GETDAYSTATE</a> notification code, which is sent whenever the control needs to be refreshed.

The array at 
				<i>lpDayStateArray</i> must contain as many elements as the value returned by the following macro: 

<code>MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);</code>

The preceding macro returns the total number of months that are in complete or partial view within the month calendar's display. 

Keep in mind that the array at 
				<i>lpDayStateArray</i> must contain <a href="https://msdn.microsoft.com/en-us/library/Bb760915(v=VS.85).aspx">MONTHDAYSTATE</a> values that correspond with all months currently in the control's display, in chronological order. This includes the two months that may be  partially displayed before the first month and after the last month.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb760921(v=VS.85).aspx">Using Month Calendar Controls</a>
 

 

