---
UID: NF:commctrl.MonthCal_SetDayState
title: MonthCal_SetDayState macro
author: windows-sdk-content
description: Sets the day states for all months that are currently visible within a month calendar control. You can use this macro or send the MCM_SETDAYSTATE message explicitly.
old-location: controls\MonthCal_SetDayState.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setdaystate.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
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
---

# MonthCal_SetDayState macro


## -description


Sets the day states for all months that are currently visible within a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/518cb2a9-ea82-40b4-88ca-f901b6f9f8c4">MCM_SETDAYSTATE</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


### -param cbds

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Value of type <b>int</b> indicating how many elements are in the array that <i>lpDayStateArray</i> points to. 


### -param rgds

Type: <b>LPMONTHDAYSTATE</b>

Pointer to an array of <a href="https://msdn.microsoft.com/eb3dd6cb-738e-424b-945b-1485798a444c">MONTHDAYSTATE</a> values that define how the month calendar control will draw each day in its display. 


## -remarks



An application can explicitly set day state information by using this macro, but the state will not persist when a different part of the calendar is scrolled into view. Day state information is usually set in response to the <a href="https://msdn.microsoft.com/dc2608e0-c598-4b26-9195-208f09cd84b7">MCN_GETDAYSTATE</a> notification code, which is sent whenever the control needs to be refreshed.

The array at 
				<i>lpDayStateArray</i> must contain as many elements as the value returned by the following macro: 

<code>MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);</code>

The preceding macro returns the total number of months that are in complete or partial view within the month calendar's display. 

Keep in mind that the array at 
				<i>lpDayStateArray</i> must contain <a href="https://msdn.microsoft.com/eb3dd6cb-738e-424b-945b-1485798a444c">MONTHDAYSTATE</a> values that correspond with all months currently in the control's display, in chronological order. This includes the two months that may be  partially displayed before the first month and after the last month.




## -see-also




<a href="https://msdn.microsoft.com/d27d8f11-b400-409e-a9bf-65c0a79093b4">Using Month Calendar Controls</a>
 

 

