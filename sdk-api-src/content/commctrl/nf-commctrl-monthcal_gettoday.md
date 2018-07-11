---
UID: NF:commctrl.MonthCal_GetToday
title: MonthCal_GetToday macro
author: windows-sdk-content
description: Retrieves the date information for the date specified as &#0034;today&#0034; for a month calendar control. You can use this macro or send the MCM_GETTODAY message explicitly.
old-location: controls\MonthCal_GetToday.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_gettoday.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: MonthCal_GetToday, MonthCal_GetToday macro [Windows Controls], _win32_MonthCal_GetToday, _win32_MonthCal_GetToday_cpp, commctrl/MonthCal_GetToday, controls.MonthCal_GetToday, controls._win32_MonthCal_GetToday
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
 - MonthCal_GetToday
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_GetToday macro


## -description


Retrieves the date information for the date specified as "today" for a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/a79feb57-6aa3-4c96-95f3-7018b6b8327f">MCM_GETTODAY</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param pst

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


#### - lpToday

Type: <b>LPSYSTEMTIME</b>

Pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that will receive the date information. The time members of this structure will not be modified. This parameter must be a valid address and cannot be <b>NULL</b>. 

