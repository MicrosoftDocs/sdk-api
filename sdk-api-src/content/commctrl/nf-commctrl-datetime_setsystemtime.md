---
UID: NF:commctrl.DateTime_SetSystemtime
title: DateTime_SetSystemtime macro
author: windows-sdk-content
description: Sets a date and time picker (DTP) control to a given date and time. You can use this macro or send the DTM_SETSYSTEMTIME message explicitly.
old-location: controls\DateTime_SetSystemtime.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setsystemtime.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DateTime_SetSystemtime, DateTime_SetSystemtime macro [Windows Controls], GDT_NONE, GDT_VALID, _win32_DateTime_SetSystemtime, _win32_DateTime_SetSystemtime_cpp, commctrl/DateTime_SetSystemtime, controls.DateTime_SetSystemtime, controls._win32_DateTime_SetSystemtime
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
 - DateTime_SetSystemtime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- DateTime_SetSystemtime
: 
---

# DateTime_SetSystemtime macro


## -description


Sets a date and time picker (DTP) control to a given date and time. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761782(v=VS.85).aspx">DTM_SETSYSTEMTIME</a> message explicitly. 


## -parameters




### -param hdp

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to a DTP control. 


### -param gd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD</a></b>

A value that specifies the action that should be performed. This should be set to one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GDT_VALID"></a><a id="gdt_valid"></a><dl>
<dt><b>GDT_VALID</b></dt>
</dl>
</td>
<td width="60%">
Set the DTP control according to the data within the <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure pointed to by <i>lpSysTime</i>. 

</td>
</tr>
<tr>
<td width="40%"><a id="GDT_NONE"></a><a id="gdt_none"></a><dl>
<dt><b>GDT_NONE</b></dt>
</dl>
</td>
<td width="60%">
Set the DTP control to "no date" and clear its check box. When this flag is specified, 
						<i>lpSysTime</i> is ignored. This flag applies only to DTP controls that are set to the <a href="https://msdn.microsoft.com/en-us/library/Bb761728(v=VS.85).aspx">DTS_SHOWNONE</a> style. 

</td>
</tr>
</table>
 


### -param pst

Type: <b>LPSYSTEMTIME</b>

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the system time information by which to set the DTP control. 

