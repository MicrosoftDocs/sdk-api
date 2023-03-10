---
UID: NS:commctrl.tagMCGRIDINFO
title: MCGRIDINFO (commctrl.h)
description: Contains information about part of a calendar control.
helpviewer_keywords: ["*PMCGRIDINFO","MCGIF_DATE","MCGIF_NAME","MCGIF_RECT","MCGIP_CALENDAR","MCGIP_CALENDARBODY","MCGIP_CALENDARCELL","MCGIP_CALENDARCONTROL","MCGIP_CALENDARHEADER","MCGIP_CALENDARROW","MCGIP_FOOTER","MCGIP_NEXT","MCGIP_PREV","MCGRIDINFO","MCGRIDINFO structure [Windows Controls]","PMCGRIDINFO","PMCGRIDINFO structure pointer [Windows Controls]","_shell_MCGRIDINFO","_shell_MCGRIDINFO_cpp","commctrl/MCGRIDINFO","commctrl/PMCGRIDINFO","controls.MCGRIDINFO","controls._shell_MCGRIDINFO"]
old-location: controls\MCGRIDINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\structures\mcgridinfo.htm
ms.date: 12/05/2018
ms.keywords: '*PMCGRIDINFO, MCGIF_DATE, MCGIF_NAME, MCGIF_RECT, MCGIP_CALENDAR, MCGIP_CALENDARBODY, MCGIP_CALENDARCELL, MCGIP_CALENDARCONTROL, MCGIP_CALENDARHEADER, MCGIP_CALENDARROW, MCGIP_FOOTER, MCGIP_NEXT, MCGIP_PREV, MCGRIDINFO, MCGRIDINFO structure [Windows Controls], PMCGRIDINFO, PMCGRIDINFO structure pointer [Windows Controls], _shell_MCGRIDINFO, _shell_MCGRIDINFO_cpp, commctrl/MCGRIDINFO, commctrl/PMCGRIDINFO, controls.MCGRIDINFO, controls._shell_MCGRIDINFO'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MCGRIDINFO, *PMCGRIDINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMCGRIDINFO
 - commctrl/tagMCGRIDINFO
 - PMCGRIDINFO
 - commctrl/PMCGRIDINFO
 - MCGRIDINFO
 - commctrl/MCGRIDINFO
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
 - MCGRIDINFO
---

# MCGRIDINFO structure


## -description

Contains information about part of a calendar control.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of this structure, in bytes.

### -field dwPart

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The part of the calendar control for which information is being requested. One of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MCGIP_CALENDARCONTROL"></a><a id="mcgip_calendarcontrol"></a><dl>
<dt><b>MCGIP_CALENDARCONTROL</b></dt>
</dl>
</td>
<td width="60%">
The entire calendar control, which may include up to 12 calendars.

</td>
</tr>
<tr>
<td width="40%"><a id="MCGIP_NEXT"></a><a id="mcgip_next"></a><dl>
<dt><b>MCGIP_NEXT</b></dt>
</dl>
</td>
<td width="60%">
The next button.

</td>
</tr>
<tr>
<td width="40%"><a id="MCGIP_PREV"></a><a id="mcgip_prev"></a><dl>
<dt><b>MCGIP_PREV</b></dt>
</dl>
</td>
<td width="60%">
The previous button.

</td>
</tr>
<tr>
<td width="40%"><a id="MCGIP_FOOTER"></a><a id="mcgip_footer"></a><dl>
<dt><b>MCGIP_FOOTER</b></dt>
</dl>
</td>
<td width="60%">
The footer.

</td>
</tr>
<tr>
<td width="40%"><a id="MCGIP_CALENDAR"></a><a id="mcgip_calendar"></a><dl>
<dt><b>MCGIP_CALENDAR</b></dt>
</dl>
</td>
<td width="60%">
One specific calendar. Used with <b>iCalendar</b> and <b>pszName</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MCGIP_CALENDARHEADER"></a><a id="mcgip_calendarheader"></a><dl>
<dt><b>MCGIP_CALENDARHEADER</b></dt>
</dl>
</td>
<td width="60%">
Calendar header. Used with <b>iCalendar</b> and <b>pszName</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MCGIP_CALENDARBODY"></a><a id="mcgip_calendarbody"></a><dl>
<dt><b>MCGIP_CALENDARBODY</b></dt>
</dl>
</td>
<td width="60%">
Calendar body. Used with <b>iCalendar</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MCGIP_CALENDARROW"></a><a id="mcgip_calendarrow"></a><dl>
<dt><b>MCGIP_CALENDARROW</b></dt>
</dl>
</td>
<td width="60%">
A given calendar row.  Used with <b>iCalendar</b> and <b>iRow</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MCGIP_CALENDARCELL"></a><a id="mcgip_calendarcell"></a><dl>
<dt><b>MCGIP_CALENDARCELL</b></dt>
</dl>
</td>
<td width="60%">
A given calendar cell. Used with <b>iCalendar</b>, <b>iRow</b>, <b>iCol</b>, <b>bSelected</b> and <b>pszName</b>.

</td>
</tr>
</table>

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Indicates what information is to be filled in. A combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MCGIF_DATE"></a><a id="mcgif_date"></a><dl>
<dt><b>MCGIF_DATE</b></dt>
</dl>
</td>
<td width="60%">
<b>stStart</b> and <b>stEnd</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MCGIF_RECT"></a><a id="mcgif_rect"></a><dl>
<dt><b>MCGIF_RECT</b></dt>
</dl>
</td>
<td width="60%">
<b>rc</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MCGIF_NAME"></a><a id="mcgif_name"></a><dl>
<dt><b>MCGIF_NAME</b></dt>
</dl>
</td>
<td width="60%">
<b>pszName</b>.

</td>
</tr>
</table>

### -field iCalendar

Type: <b>int</b>

If <b>dwPart</b> is MCGIP_CALENDAR, MCGIP_CALENDARHEADER, MCGIP_CALENDARBODY, MCGIP_CALENDARROW, or MCGIP_CALENDARCELL, this member specifies the index of the calendar for which to retrieve information. For those parts, this must be a valid value even if there is only one calendar that is currently in the control.

### -field iRow

Type: <b>int</b>

If <b>dwPart</b> is MCGIP_CALENDARROW, specifies the row for which to return information.

### -field iCol

Type: <b>int</b>

If <b>dwPart</b> is MCGIP_CALENDARCELL, specifies the column of the cell for which to return information. The <b>iRow</b> member provides the row of the cell for which to return information.

### -field bSelected

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If <b>dwPart</b> is MCGIP_CALENDARCELL, indicates if the cell described by <b>iRow</b> and <b>iCol</b> is currently selected.

### -field stStart

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

Returns the start date specified by iCalendar. Used only when <b>dwFlags</b> contains MCGIF_DATE.

### -field stEnd

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

Returns the end date specified by iCalendar. Used only when <b>dwFlags</b> contains MCGIF_DATE.

### -field rc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

Returns the rectangle of the part specified in <b>dwPart</b>. Set only if <b>dwFlags</b> contains MCGIF_RECT.

### -field pszName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

Pointer to a string for which <b>cchName</b> is the length. Set only if <b>dwFlags</b> contains MCGIF_NAME, and only for the following parts, as described in the <b>dwPart</b> member.
                

<ul>
<li>MCGIP_CALENDAR: Returns the text of the selected dates. In the case of multiple selection, returns the date at the start of the selection.</li>
<li>MCGIP_CALENDARCELL: Returns the text of the cell indicated by <b>iRow</b> and <b>iCol</b>, for instance "11" if the 11th day was specified.</li>
<li>MCGIP_CALENDARHEADER: Returns the text of what it says in the calendar header, for instance "July, 2006".</li>
</ul>

### -field cchName

Type: <b>size_t</b>

Length of <b>pszName</b>, in characters.