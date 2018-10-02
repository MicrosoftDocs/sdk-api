---
UID: NF:commctrl.MonthCal_GetRange
title: MonthCal_GetRange macro
author: windows-sdk-content
description: Retrieves the minimum and maximum allowable dates set for a month calendar control. You can use this macro or send the MCM_GETRANGE message explicitly.
old-location: controls\MonthCal_GetRange.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getrange.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: MonthCal_GetRange, MonthCal_GetRange macro [Windows Controls], _win32_MonthCal_GetRange, _win32_MonthCal_GetRange_cpp, commctrl/MonthCal_GetRange, controls.MonthCal_GetRange, controls._win32_MonthCal_GetRange
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
 - MonthCal_GetRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MonthCal_GetRange macro


## -description


Retrieves the minimum and maximum allowable dates set for a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760983(v=VS.85).aspx">MCM_GETRANGE</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to a month calendar control. 


### -param rgst

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structures that will receive the date limit information. The minimum limit is set in <i>lprgSysTimeArray</i>[0], and <i>lprgSysTimeArray</i>[1] receives the maximum limit. If either element is set to all zeros, then no corresponding limit is set for the month calendar control. The time members of these structures will not be modified. This parameter must be a valid address and cannot be <b>NULL</b>. 

