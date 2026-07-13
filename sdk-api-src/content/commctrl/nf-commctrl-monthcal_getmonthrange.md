---
UID: NF:commctrl.MonthCal_GetMonthRange
title: MonthCal_GetMonthRange macro (commctrl.h)
description: Retrieves date information (using SYSTEMTIME structures) that represents the high and low limits of a month calendar control's display. You can use this macro or send the MCM_GETMONTHRANGE message explicitly.
helpviewer_keywords: ["GMR_DAYSTATE","GMR_VISIBLE","MonthCal_GetMonthRange","MonthCal_GetMonthRange macro [Windows Controls]","_win32_MonthCal_GetMonthRange","_win32_MonthCal_GetMonthRange_cpp","commctrl/MonthCal_GetMonthRange","controls.MonthCal_GetMonthRange","controls._win32_MonthCal_GetMonthRange"]
old-location: controls\MonthCal_GetMonthRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getmonthrange.htm
ms.date: 10/21/2024
ms.keywords: GMR_DAYSTATE, GMR_VISIBLE, MonthCal_GetMonthRange, MonthCal_GetMonthRange macro [Windows Controls], _win32_MonthCal_GetMonthRange, _win32_MonthCal_GetMonthRange_cpp, commctrl/MonthCal_GetMonthRange, controls.MonthCal_GetMonthRange, controls._win32_MonthCal_GetMonthRange
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
 - MonthCal_GetMonthRange
 - commctrl/MonthCal_GetMonthRange
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
 - MonthCal_GetMonthRange
---

# MonthCal_GetMonthRange macro

## -syntax

```cpp
INT MonthCal_GetMonthRange(
   HWND         hmc,
   DWORD        gmr,
   LPSYSTEMTIME rgst
);
```

## -returns

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

Returns an INT value that represents the range, in months, spanned by the two limits returned at <i>rgst</i>.


## -description

Retrieves date information (using <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structures) that represents the high and low limits of a month calendar control's display. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getmonthrange">MCM_GETMONTHRANGE</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param gmr

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

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

### -param rgst

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structures that will receive the lower and upper limits of the scope specified by <i>gmr</i>. The lower and upper limits are placed in rgst[0] and rgst[1], respectively. The time members of these structures will not be modified. This parameter must be a valid address and cannot be <b>NULL</b>.
