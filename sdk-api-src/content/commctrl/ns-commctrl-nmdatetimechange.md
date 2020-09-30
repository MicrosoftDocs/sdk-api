---
UID: NS:commctrl.tagNMDATETIMECHANGE
title: NMDATETIMECHANGE (commctrl.h)
description: Contains information about a change that has taken place in a date and time picker (DTP) control. This structure is used with the DTN_DATETIMECHANGE notification code.
helpviewer_keywords: ["*LPNMDATETIMECHANGE","GDT_NONE","GDT_VALID","LPNMDATETIMECHANGE","LPNMDATETIMECHANGE structure pointer [Windows Controls]","NMDATETIMECHANGE","NMDATETIMECHANGE structure [Windows Controls]","_win32_NMDATETIMECHANGE","_win32_NMDATETIMECHANGE_cpp","commctrl/LPNMDATETIMECHANGE","commctrl/NMDATETIMECHANGE","controls.NMDATETIMECHANGE","controls._win32_NMDATETIMECHANGE"]
old-location: controls\NMDATETIMECHANGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\structures\nmdatetimechange.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMDATETIMECHANGE, GDT_NONE, GDT_VALID, LPNMDATETIMECHANGE, LPNMDATETIMECHANGE structure pointer [Windows Controls], NMDATETIMECHANGE, NMDATETIMECHANGE structure [Windows Controls], _win32_NMDATETIMECHANGE, _win32_NMDATETIMECHANGE_cpp, commctrl/LPNMDATETIMECHANGE, commctrl/NMDATETIMECHANGE, controls.NMDATETIMECHANGE, controls._win32_NMDATETIMECHANGE'
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
req.typenames: NMDATETIMECHANGE, *LPNMDATETIMECHANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMDATETIMECHANGE
 - commctrl/tagNMDATETIMECHANGE
 - LPNMDATETIMECHANGE
 - commctrl/LPNMDATETIMECHANGE
 - NMDATETIMECHANGE
 - commctrl/NMDATETIMECHANGE
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
 - NMDATETIMECHANGE
---

# NMDATETIMECHANGE structure


## -description

Contains information about a change that has taken place in a date and time picker (DTP) control. This structure is used with the <a href="/windows/desktop/Controls/dtn-datetimechange">DTN_DATETIMECHANGE</a> notification code.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about the notification code.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A value that indicates if the control was set to "no date" status (for <a href="/windows/desktop/Controls/date-and-time-picker-control-styles">DTS_SHOWNONE</a> only). This flag also specifies whether the contents of the <b>st</b> member are valid and contain current time information. This value can be one of the following: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GDT_NONE"></a><a id="gdt_none"></a><dl>
<dt><b>GDT_NONE</b></dt>
</dl>
</td>
<td width="60%">
The control is set to "no date" status. The "no date" status applies only to controls that are set to the <a href="/windows/desktop/Controls/date-and-time-picker-control-styles">DTS_SHOWNONE</a> style.

</td>
</tr>
<tr>
<td width="40%"><a id="GDT_VALID"></a><a id="gdt_valid"></a><dl>
<dt><b>GDT_VALID</b></dt>
</dl>
</td>
<td width="60%">
The control is not set to the "no date" status. The 
						<b>st</b> member contains the current date and time.

</td>
</tr>
</table>

### -field st

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains information about the current system date and time.