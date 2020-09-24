---
UID: NF:commctrl.MonthCal_SetFirstDayOfWeek
title: MonthCal_SetFirstDayOfWeek macro (commctrl.h)
description: Sets the first day of the week for a month calendar control. You can use this macro or send the MCM_SETFIRSTDAYOFWEEK message explicitly.
helpviewer_keywords: ["MonthCal_SetFirstDayOfWeek","MonthCal_SetFirstDayOfWeek macro [Windows Controls]","_win32_MonthCal_SetFirstDayOfWeek","_win32_MonthCal_SetFirstDayOfWeek_cpp","commctrl/MonthCal_SetFirstDayOfWeek","controls.MonthCal_SetFirstDayOfWeek","controls._win32_MonthCal_SetFirstDayOfWeek"]
old-location: controls\MonthCal_SetFirstDayOfWeek.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setfirstdayofweek.htm
ms.date: 12/05/2018
ms.keywords: MonthCal_SetFirstDayOfWeek, MonthCal_SetFirstDayOfWeek macro [Windows Controls], _win32_MonthCal_SetFirstDayOfWeek, _win32_MonthCal_SetFirstDayOfWeek_cpp, commctrl/MonthCal_SetFirstDayOfWeek, controls.MonthCal_SetFirstDayOfWeek, controls._win32_MonthCal_SetFirstDayOfWeek
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
 - MonthCal_SetFirstDayOfWeek
 - commctrl/MonthCal_SetFirstDayOfWeek
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
 - MonthCal_SetFirstDayOfWeek
---

# MonthCal_SetFirstDayOfWeek macro


## -description

Sets the first day of the week for a month calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-setfirstdayofweek">MCM_SETFIRSTDAYOFWEEK</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param iDay

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Value of type <b>int</b> that specifies which day is to be set as the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.

## -remarks

If the first day of the week is set to anything other than the default (LOCALE_IFIRSTDAYOFWEEK), the control will not automatically update first-day-of-the-week changes based on locale changes.