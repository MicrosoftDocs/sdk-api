---
UID: NF:commctrl.MonthCal_SetFirstDayOfWeek
title: MonthCal_SetFirstDayOfWeek macro
author: windows-driver-content
description: Sets the first day of the week for a month calendar control. You can use this macro or send the MCM_SETFIRSTDAYOFWEEK message explicitly.
old-location: controls\MonthCal_SetFirstDayOfWeek.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setfirstdayofweek.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: MonthCal_SetFirstDayOfWeek, MonthCal_SetFirstDayOfWeek macro [Windows Controls], _win32_MonthCal_SetFirstDayOfWeek, _win32_MonthCal_SetFirstDayOfWeek_cpp, commctrl/MonthCal_SetFirstDayOfWeek, controls.MonthCal_SetFirstDayOfWeek, controls._win32_MonthCal_SetFirstDayOfWeek
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	MonthCal_SetFirstDayOfWeek
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_SetFirstDayOfWeek macro


## -description


Sets the first day of the week for a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/6e0dc906-a41e-4c3a-9528-1f5428dceb8d">MCM_SETFIRSTDAYOFWEEK</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param iDay

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Value of type <b>int</b> that specifies which day is to be set as the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.


#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


## -remarks



If the first day of the week is set to anything other than the default (LOCALE_IFIRSTDAYOFWEEK), the control will not automatically update first-day-of-the-week changes based on locale changes. 



