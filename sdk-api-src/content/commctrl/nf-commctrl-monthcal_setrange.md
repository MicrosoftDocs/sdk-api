---
UID: NF:commctrl.MonthCal_SetRange
title: MonthCal_SetRange macro (commctrl.h)
description: Sets the minimum and maximum allowable dates for a month calendar control. You can use this macro or send the MCM_SETRANGE message explicitly.
helpviewer_keywords: ["GDTR_MAX","GDTR_MIN","MonthCal_SetRange","MonthCal_SetRange macro [Windows Controls]","_win32_MonthCal_SetRange","_win32_MonthCal_SetRange_cpp","commctrl/MonthCal_SetRange","controls.MonthCal_SetRange","controls._win32_MonthCal_SetRange"]
old-location: controls\MonthCal_SetRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setrange.htm
ms.date: 10/21/2024
ms.keywords: GDTR_MAX, GDTR_MIN, MonthCal_SetRange, MonthCal_SetRange macro [Windows Controls], _win32_MonthCal_SetRange, _win32_MonthCal_SetRange_cpp, commctrl/MonthCal_SetRange, controls.MonthCal_SetRange, controls._win32_MonthCal_SetRange
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
 - MonthCal_SetRange
 - commctrl/MonthCal_SetRange
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
 - MonthCal_SetRange
---

# MonthCal_SetRange macro

## -syntax

```cpp
BOOL MonthCal_SetRange(
   HWND         hmc,
   DWORD        gd,
   LPSYSTEMTIME rgst
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Sets the minimum and maximum allowable dates for a month calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-setrange">MCM_SETRANGE</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param gd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

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
The maximum allowable date is being set. The <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure at <i>rgst</i>[1] must contain date information. 

</td>
</tr>
<tr>
<td width="40%"><a id="GDTR_MIN"></a><a id="gdtr_min"></a><dl>
<dt><b>GDTR_MIN</b></dt>
</dl>
</td>
<td width="60%">
The minimum allowable date is being set. The <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure at <i>rgst</i>[0] must contain date information. 

</td>
</tr>
</table>

### -param rgst

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structures that contain the date limits. The maximum limit must be in <i>rgst</i>[1] if GDTR_MAX is specified, and <i>rgst</i>[0] must contain the minimum limit if GDTR_MIN is specified.
