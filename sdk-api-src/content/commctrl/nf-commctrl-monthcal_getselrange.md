---
UID: NF:commctrl.MonthCal_GetSelRange
title: MonthCal_GetSelRange macro (commctrl.h)
author: windows-sdk-content
description: Retrieves date information that represents the upper and lower limits of the date range currently selected by the user. You can use this macro or send the MCM_GETSELRANGE message explicitly.
old-location: controls\MonthCal_GetSelRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getselrange.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MonthCal_GetSelRange, MonthCal_GetSelRange macro [Windows Controls], _win32_MonthCal_GetSelRange, _win32_MonthCal_GetSelRange_cpp, commctrl/MonthCal_GetSelRange, controls.MonthCal_GetSelRange, controls._win32_MonthCal_GetSelRange
ms.topic: macro
f1_keywords: 
 - "commctrl/MonthCal_GetSelRange"
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
 - MonthCal_GetSelRange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MonthCal_GetSelRange macro


## -description


Retrieves date information that represents the upper and lower limits of the date range currently selected by the user. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcm-getselrange">MCM_GETSELRANGE</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control. 


### -param rgst

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structures that will receive the lower and upper limits of the user's selection. The lower and upper limits are placed in <i>lprgSysTimeArray</i>[0] and <i>lprgSysTimeArray</i>[1], respectively. The time members of these structures will not be modified. This parameter must be a valid address and cannot be <b>NULL</b>. 

