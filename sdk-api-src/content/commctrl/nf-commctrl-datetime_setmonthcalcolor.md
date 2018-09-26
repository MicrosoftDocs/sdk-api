---
UID: NF:commctrl.DateTime_SetMonthCalColor
title: DateTime_SetMonthCalColor macro
author: windows-sdk-content
description: Sets the color for a given portion of the month calendar within a date and time picker (DTP) control. You can use this macro or send the DTM_SETMCCOLOR message explicitly.
old-location: controls\DateTime_SetMonthCalColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setmonthcalcolor.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DateTime_SetMonthCalColor, DateTime_SetMonthCalColor macro [Windows Controls], MCSC_BACKGROUND, MCSC_MONTHBK, MCSC_TEXT, MCSC_TITLEBK, MCSC_TITLETEXT, MCSC_TRAILINGTEXT, _win32_DateTime_SetMonthCalColor, _win32_DateTime_SetMonthCalColor_cpp, commctrl/DateTime_SetMonthCalColor, controls.DateTime_SetMonthCalColor, controls._win32_DateTime_SetMonthCalColor
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
 - DateTime_SetMonthCalColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DateTime_SetMonthCalColor macro


## -description


Sets the color for a given portion of the month calendar within a date and time picker (DTP) control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761773(v=VS.85).aspx">DTM_SETMCCOLOR</a> message explicitly. 


## -parameters




### -param hdp

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to a DTP control. 


### -param iColor

Type: <b>int</b>

A value of type <b>int</b> specifying which month calendar color to set. This value can be one of the following: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MCSC_BACKGROUND"></a><a id="mcsc_background"></a><dl>
<dt><b>MCSC_BACKGROUND</b></dt>
</dl>
</td>
<td width="60%">
Set the background color displayed between months.

</td>
</tr>
<tr>
<td width="40%"><a id="MCSC_MONTHBK"></a><a id="mcsc_monthbk"></a><dl>
<dt><b>MCSC_MONTHBK</b></dt>
</dl>
</td>
<td width="60%">
Set the background color displayed within the month.

</td>
</tr>
<tr>
<td width="40%"><a id="MCSC_TEXT"></a><a id="mcsc_text"></a><dl>
<dt><b>MCSC_TEXT</b></dt>
</dl>
</td>
<td width="60%">
Set the color used to display text within a month.

</td>
</tr>
<tr>
<td width="40%"><a id="MCSC_TITLEBK"></a><a id="mcsc_titlebk"></a><dl>
<dt><b>MCSC_TITLEBK</b></dt>
</dl>
</td>
<td width="60%">
Set the background color displayed in the calendar's title.

</td>
</tr>
<tr>
<td width="40%"><a id="MCSC_TITLETEXT"></a><a id="mcsc_titletext"></a><dl>
<dt><b>MCSC_TITLETEXT</b></dt>
</dl>
</td>
<td width="60%">
Set the color used to display text within the calendar's title.

</td>
</tr>
<tr>
<td width="40%"><a id="MCSC_TRAILINGTEXT"></a><a id="mcsc_trailingtext"></a><dl>
<dt><b>MCSC_TRAILINGTEXT</b></dt>
</dl>
</td>
<td width="60%">
Set the color used to display header day and trailing day text. Header and trailing days are the days from the previous and following months that appear on the current month calendar.

</td>
</tr>
</table>
 


### -param clr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">COLORREF</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Dd183449(v=VS.85).aspx">COLORREF</a> value that represents the color that will be set for the specified area of the month calendar. 


## -remarks



When visual styles are enabled, this macro has no effect except when <i>iColor</i> is MCSC_BACKGROUND.	



