---
UID: NF:commctrl.MonthCal_GetToday
title: MonthCal_GetToday macro (commctrl.h)
description: Retrieves the date information for the date specified as &#0034;today&#0034; for a month calendar control. You can use this macro or send the MCM_GETTODAY message explicitly.helpviewer_keywords: ["MonthCal_GetToday","MonthCal_GetToday macro [Windows Controls]","_win32_MonthCal_GetToday","_win32_MonthCal_GetToday_cpp","commctrl/MonthCal_GetToday","controls.MonthCal_GetToday","controls._win32_MonthCal_GetToday"]
old-location: controls\MonthCal_GetToday.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_gettoday.htm
ms.date: 12/05/2018
ms.keywords: MonthCal_GetToday, MonthCal_GetToday macro [Windows Controls], _win32_MonthCal_GetToday, _win32_MonthCal_GetToday_cpp, commctrl/MonthCal_GetToday, controls.MonthCal_GetToday, controls._win32_MonthCal_GetToday
f1_keywords:
- commctrl/MonthCal_GetToday
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
- MonthCal_GetToday
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MonthCal_GetToday macro


## -description


Retrieves the date information for the date specified as "today" for a month calendar control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcm-gettoday">MCM_GETTODAY</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control. 


### -param pst

Type: <b>LPSYSTEMTIME</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that will receive the date information. The time members of this structure will not be modified. This parameter must be a valid address and cannot be <b>NULL</b>. 

