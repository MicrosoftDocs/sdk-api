---
UID: NS:commctrl.MCHITTESTINFO
title: MCHITTESTINFO (commctrl.h)
description: Carries information specific to hit-testing points for a month calendar control. This structure is used with the MCM_HITTEST message and the corresponding MonthCal_HitTest macro.
helpviewer_keywords: ["*PMCHITTESTINFO","MCHITTESTINFO","MCHITTESTINFO structure [Windows Controls]","MCHT_CALENDARBK","MCHT_CALENDARCONTROL","MCHT_CALENDARDATE","MCHT_CALENDARDATEMAX","MCHT_CALENDARDATEMIN","MCHT_CALENDARDATENEXT","MCHT_CALENDARDATEPREV","MCHT_CALENDARDAY","MCHT_CALENDARWEEKNUM","MCHT_NOWHERE","MCHT_TITLEBK","MCHT_TITLEBTNNEXT","MCHT_TITLEBTNPREV","MCHT_TITLEMONTH","MCHT_TITLEYEAR","PMCHITTESTINFO","PMCHITTESTINFO structure pointer [Windows Controls]","_win32_MCHITTESTINFO","_win32_MCHITTESTINFO_cpp","commctrl/MCHITTESTINFO","commctrl/PMCHITTESTINFO","controls.MCHITTESTINFO","controls._win32_MCHITTESTINFO"]
old-location: controls\MCHITTESTINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\structures\mchittestinfo.htm
ms.date: 12/05/2018
ms.keywords: '*PMCHITTESTINFO, MCHITTESTINFO, MCHITTESTINFO structure [Windows Controls], MCHT_CALENDARBK, MCHT_CALENDARCONTROL, MCHT_CALENDARDATE, MCHT_CALENDARDATEMAX, MCHT_CALENDARDATEMIN, MCHT_CALENDARDATENEXT, MCHT_CALENDARDATEPREV, MCHT_CALENDARDAY, MCHT_CALENDARWEEKNUM, MCHT_NOWHERE, MCHT_TITLEBK, MCHT_TITLEBTNNEXT, MCHT_TITLEBTNPREV, MCHT_TITLEMONTH, MCHT_TITLEYEAR, PMCHITTESTINFO, PMCHITTESTINFO structure pointer [Windows Controls], _win32_MCHITTESTINFO, _win32_MCHITTESTINFO_cpp, commctrl/MCHITTESTINFO, commctrl/PMCHITTESTINFO, controls.MCHITTESTINFO, controls._win32_MCHITTESTINFO'
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
req.typenames: MCHITTESTINFO, *PMCHITTESTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMCHITTESTINFO
 - commctrl/PMCHITTESTINFO
 - MCHITTESTINFO
 - commctrl/MCHITTESTINFO
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
 - MCHITTESTINFO
---

# MCHITTESTINFO structure


## -description

Carries information specific to hit-testing points for a month calendar control. This structure is used with the <a href="/windows/desktop/Controls/mcm-hittest">MCM_HITTEST</a> message and the corresponding <a href="/windows/desktop/api/commctrl/nf-commctrl-monthcal_hittest">MonthCal_HitTest</a> macro.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of this structure, in bytes.

### -field pt

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

Point to be hit-tested.

### -field uHit

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Output member that receives a bit flag representing the result of the hit-test operation. This value will be one of the following: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MCHT_CALENDARBK"></a><a id="mcht_calendarbk"></a><dl>
<dt><b>MCHT_CALENDARBK</b></dt>
</dl>
</td>
<td width="60%">
The given point was in the calendar's background.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_CALENDARCONTROL"></a><a id="mcht_calendarcontrol"></a><dl>
<dt><b>MCHT_CALENDARCONTROL</b></dt>
</dl>
</td>
<td width="60%">
The given point is outside of any calendar but within the calendar controls <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_CALENDARDATE"></a><a id="mcht_calendardate"></a><dl>
<dt><b>MCHT_CALENDARDATE</b></dt>
</dl>
</td>
<td width="60%">
The given point was on a particular date within the calendar. The <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure at <i>lpMCHitTest</i>&gt;st is set to the date at the given point.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_CALENDARDATEMIN"></a><a id="mcht_calendardatemin"></a><dl>
<dt><b>MCHT_CALENDARDATEMIN</b></dt>
</dl>
</td>
<td width="60%">
The given point was over the minimum date(s) in the calendar.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_CALENDARDATEMAX"></a><a id="mcht_calendardatemax"></a><dl>
<dt><b>MCHT_CALENDARDATEMAX</b></dt>
</dl>
</td>
<td width="60%">
 The given point was over the maximum date(s) in the calendar.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_CALENDARDATENEXT"></a><a id="mcht_calendardatenext"></a><dl>
<dt><b>MCHT_CALENDARDATENEXT</b></dt>
</dl>
</td>
<td width="60%">
The given point was over a date from the next month (partially displayed at the end of the currently displayed month). If the user clicks here, the month calendar will scroll its display to the next month or set of months.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_CALENDARDATEPREV"></a><a id="mcht_calendardateprev"></a><dl>
<dt><b>MCHT_CALENDARDATEPREV</b></dt>
</dl>
</td>
<td width="60%">
The given point was over a date from the previous month (partially displayed at the end of the currently displayed month). If the user clicks here, the month calendar will scroll its display to the previous month or set of months.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_CALENDARDAY"></a><a id="mcht_calendarday"></a><dl>
<dt><b>MCHT_CALENDARDAY</b></dt>
</dl>
</td>
<td width="60%">
The given point was over a day abbreviation ("Fri", for example). The <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure at 
						<i>lpMCHitTest</i>&gt;st is set to the corresponding date in the top row.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_CALENDARWEEKNUM"></a><a id="mcht_calendarweeknum"></a><dl>
<dt><b>MCHT_CALENDARWEEKNUM</b></dt>
</dl>
</td>
<td width="60%">
The given point was over a week number (<a href="/windows/desktop/Controls/month-calendar-control-styles">MCS_WEEKNUMBERS</a> style only). The <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure at 
						<i>lpMCHitTest</i>&gt;st is set to the corresponding date in the leftmost column.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_NOWHERE"></a><a id="mcht_nowhere"></a><dl>
<dt><b>MCHT_NOWHERE</b></dt>
</dl>
</td>
<td width="60%">
The given point was not on the month calendar control, or it was in an inactive portion of the control.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_TITLEBK"></a><a id="mcht_titlebk"></a><dl>
<dt><b>MCHT_TITLEBK</b></dt>
</dl>
</td>
<td width="60%">
The given point was over the background of a month's title.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_TITLEBTNNEXT"></a><a id="mcht_titlebtnnext"></a><dl>
<dt><b>MCHT_TITLEBTNNEXT</b></dt>
</dl>
</td>
<td width="60%">
The given point was over the button at the top right corner of the control. If the user clicks here, the month calendar will scroll its display to the next month or set of months.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_TITLEBTNPREV"></a><a id="mcht_titlebtnprev"></a><dl>
<dt><b>MCHT_TITLEBTNPREV</b></dt>
</dl>
</td>
<td width="60%">
The given point was over the button at the top left corner of the control. If the user clicks here, the month calendar will scroll its display to the previous month or set of months.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_TITLEMONTH"></a><a id="mcht_titlemonth"></a><dl>
<dt><b>MCHT_TITLEMONTH</b></dt>
</dl>
</td>
<td width="60%">
The given point was in a month's title bar, over a month name.

</td>
</tr>
<tr>
<td width="40%"><a id="MCHT_TITLEYEAR"></a><a id="mcht_titleyear"></a><dl>
<dt><b>MCHT_TITLEYEAR</b></dt>
</dl>
</td>
<td width="60%">
The given point was in a month's title bar, over the year value.

</td>
</tr>
</table>

### -field st

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

Receives date and time information specific to the location that was hit-tested.

### -field rc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

Hit-tested location.

### -field iOffset

Type: <b>int</b>

When displaying more than one calendar, this is the offset of the calendar at the hit-tested point (zero-based).

### -field iRow

Type: <b>int</b>

The row number for the calendar grid that the given hit point was over.  Example: If you hit-tested the 8th of a month, which is in the second week of the month, <b>iRow</b> will be one since the index of the row is zero-based row index.

### -field iCol

Type: <b>int</b>

The column number for the calendar grid that the given point was over. For example, if your week starts on Sunday and the 1st of the month is Friday, hit testing the 1st will return five (5) for <b>iCol</b>, since Friday is in the fifth column from the beginning of the row, using a zero-based column index.

## -remarks

Columns and rows in this control use a zero-based index system, that is, the first column or row has an index of zero.

