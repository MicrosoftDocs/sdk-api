---
UID: NF:commctrl.MonthCal_SetToday
title: MonthCal_SetToday macro
author: windows-sdk-content
description: Sets the &#0034;today&#0034; selection for a month calendar control. You can use this macro or send the MCM_SETTODAY message explicitly.
old-location: controls\MonthCal_SetToday.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_settoday.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: MonthCal_SetToday, MonthCal_SetToday macro [Windows Controls], _win32_MonthCal_SetToday, _win32_MonthCal_SetToday_cpp, commctrl/MonthCal_SetToday, controls.MonthCal_SetToday, controls._win32_MonthCal_SetToday
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - MonthCal_SetToday
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_SetToday macro


## -description


Sets the "today" selection for a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/fcd4d33d-e661-4e02-8d19-666d80e1a070">MCM_SETTODAY</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param pst

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


#### - lpSysTime

Type: <b>LPSYSTEMTIME</b>

Pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the date to be set as the "today" selection for the control. If this parameter is set to <b>NULL</b>, the control returns to the default setting. The time members of this structure are ignored. If the "today" selection is set to any date other than the default, the following conditions apply:
 

<ul>
<li>The control will not automatically update the "today" selection when the time passes midnight for the current day.</li>
<li>The control will not automatically update its display based on locale changes.</li>
</ul>
