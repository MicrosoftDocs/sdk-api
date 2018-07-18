---
UID: NF:commctrl.MonthCal_GetMonthRange
title: MonthCal_GetMonthRange macro
author: windows-sdk-content
description: Retrieves date information (using SYSTEMTIME structures) that represents the high and low limits of a month calendar control's display. You can use this macro or send the MCM_GETMONTHRANGE message explicitly.
old-location: controls\MonthCal_GetMonthRange.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getmonthrange.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GMR_DAYSTATE, GMR_VISIBLE, MonthCal_GetMonthRange, MonthCal_GetMonthRange macro [Windows Controls], _win32_MonthCal_GetMonthRange, _win32_MonthCal_GetMonthRange_cpp, commctrl/MonthCal_GetMonthRange, controls.MonthCal_GetMonthRange, controls._win32_MonthCal_GetMonthRange
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
 - MonthCal_GetMonthRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_GetMonthRange macro


## -description


Retrieves date information (using <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structures) that represents the high and low limits of a month calendar control's display. You can use this macro or send the <a href="https://msdn.microsoft.com/f50ac4b7-1f58-4639-8c78-341bb33db3c3">MCM_GETMONTHRANGE</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param gmr

TBD


### -param rgst

TBD






#### - dwFlag

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Value specifying the scope of the range limits to be retrieved. This value must be one of the following: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GMR_DAYSTATE"></a><a id="gmr_daystate"></a><dl>
<dt><b>GMR_DAYSTATE</b></dt>
</dl>
</td>
<td width="60%">
Include preceding and trailing months of visible range that are only partially displayed. 

</td>
</tr>
<tr>
<td width="40%"><a id="GMR_VISIBLE"></a><a id="gmr_visible"></a><dl>
<dt><b>GMR_VISIBLE</b></dt>
</dl>
</td>
<td width="60%">
Include only those months that are entirely displayed. 

</td>
</tr>
</table>
 


#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


#### - lprgSysTimeArray

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structures that will receive the lower and upper limits of the scope specified by <i>dwFlag</i>. The lower and upper limits are placed in lprgSysTimeArray[0] and lprgSysTimeArray[1], respectively. The time members of these structures will not be modified. This parameter must be a valid address and cannot be <b>NULL</b>. 

