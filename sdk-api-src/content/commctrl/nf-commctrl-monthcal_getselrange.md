---
UID: NF:commctrl.MonthCal_GetSelRange
title: MonthCal_GetSelRange macro
author: windows-sdk-content
description: Retrieves date information that represents the upper and lower limits of the date range currently selected by the user. You can use this macro or send the MCM_GETSELRANGE message explicitly.
old-location: controls\MonthCal_GetSelRange.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getselrange.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MonthCal_GetSelRange, MonthCal_GetSelRange macro [Windows Controls], _win32_MonthCal_GetSelRange, _win32_MonthCal_GetSelRange_cpp, commctrl/MonthCal_GetSelRange, controls.MonthCal_GetSelRange, controls._win32_MonthCal_GetSelRange
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	MonthCal_GetSelRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_GetSelRange macro


## -description


Retrieves date information that represents the upper and lower limits of the date range currently selected by the user. You can use this macro or send the <a href="https://msdn.microsoft.com/a0d0a0d5-a519-4495-a87a-2438c4590e4c">MCM_GETSELRANGE</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param rgst

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


#### - lprgSysTimeArray

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structures that will receive the lower and upper limits of the user's selection. The lower and upper limits are placed in <i>lprgSysTimeArray</i>[0] and <i>lprgSysTimeArray</i>[1], respectively. The time members of these structures will not be modified. This parameter must be a valid address and cannot be <b>NULL</b>. 

