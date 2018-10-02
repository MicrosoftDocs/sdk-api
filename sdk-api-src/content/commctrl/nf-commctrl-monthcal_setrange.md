---
UID: NF:commctrl.MonthCal_SetRange
title: MonthCal_SetRange macro
author: windows-sdk-content
description: Sets the minimum and maximum allowable dates for a month calendar control. You can use this macro or send the MCM_SETRANGE message explicitly.
old-location: controls\MonthCal_SetRange.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setrange.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GDTR_MAX, GDTR_MIN, MonthCal_SetRange, MonthCal_SetRange macro [Windows Controls], _win32_MonthCal_SetRange, _win32_MonthCal_SetRange_cpp, commctrl/MonthCal_SetRange, controls.MonthCal_SetRange, controls._win32_MonthCal_SetRange
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
 - MonthCal_SetRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MonthCal_SetRange macro


## -description


Sets the minimum and maximum allowable dates for a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761012(v=VS.85).aspx">MCM_SETRANGE</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to a month calendar control. 


### -param gd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD</a></b>

Flag values that specify which date limits are being set. This value must be one or both of the following: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GDTR_MAX"></a><a id="gdtr_max"></a><dl>
<dt><b>GDTR_MAX</b></dt>
</dl>
</td>
<td width="60%">
The maximum allowable date is being set. The <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure at <i>lprgSysTimeArray</i>[1] must contain date information. 

</td>
</tr>
<tr>
<td width="40%"><a id="GDTR_MIN"></a><a id="gdtr_min"></a><dl>
<dt><b>GDTR_MIN</b></dt>
</dl>
</td>
<td width="60%">
The minimum allowable date is being set. The <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure at <i>lprgSysTimeArray</i>[0] must contain date information. 

</td>
</tr>
</table>
 


### -param rgst

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structures that contain the date limits. The maximum limit must be in <i>lprgSysTimeArray</i>[1] if GDTR_MAX is specified, and <i>lprgSysTimeArray</i>[0] must contain the minimum limit if GDTR_MIN is specified. 

