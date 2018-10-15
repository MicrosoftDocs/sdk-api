---
UID: NS:commctrl.tagNMDATETIMECHANGE
title: tagNMDATETIMECHANGE
author: windows-sdk-content
description: Contains information about a change that has taken place in a date and time picker (DTP) control. This structure is used with the DTN_DATETIMECHANGE notification code.
old-location: controls\NMDATETIMECHANGE.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\datetime\structures\nmdatetimechange.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*LPNMDATETIMECHANGE, GDT_NONE, GDT_VALID, LPNMDATETIMECHANGE, LPNMDATETIMECHANGE structure pointer [Windows Controls], NMDATETIMECHANGE, NMDATETIMECHANGE structure [Windows Controls], _win32_NMDATETIMECHANGE, _win32_NMDATETIMECHANGE_cpp, commctrl/LPNMDATETIMECHANGE, commctrl/NMDATETIMECHANGE, controls.NMDATETIMECHANGE, controls._win32_NMDATETIMECHANGE, tagNMDATETIMECHANGE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - NMDATETIMECHANGE
product: Windows
targetos: Windows
req.typenames: NMDATETIMECHANGE, *LPNMDATETIMECHANGE
req.redist: 
---

# tagNMDATETIMECHANGE structure


## -description


Contains information about a change that has taken place in a date and time picker (DTP) control. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb761737(v=VS.85).aspx">DTN_DATETIMECHANGE</a> notification code. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about the notification code. 


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A value that indicates if the control was set to "no date" status (for <a href="https://msdn.microsoft.com/en-us/library/Bb761728(v=VS.85).aspx">DTS_SHOWNONE</a> only). This flag also specifies whether the contents of the <b>st</b> member are valid and contain current time information. This value can be one of the following: 

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
The control is set to "no date" status. The "no date" status applies only to controls that are set to the <a href="https://msdn.microsoft.com/en-us/library/Bb761728(v=VS.85).aspx">DTS_SHOWNONE</a> style.

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

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>

A <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains information about the current system date and time. 

