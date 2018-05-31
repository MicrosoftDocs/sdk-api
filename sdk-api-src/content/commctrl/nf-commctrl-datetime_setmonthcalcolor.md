---
UID: NF:commctrl.DateTime_SetMonthCalColor
title: DateTime_SetMonthCalColor macro
author: windows-sdk-content
description: Sets the color for a given portion of the month calendar within a date and time picker (DTP) control. You can use this macro or send the DTM_SETMCCOLOR message explicitly.
old-location: controls\DateTime_SetMonthCalColor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setmonthcalcolor.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DateTime_SetMonthCalColor, DateTime_SetMonthCalColor macro [Windows Controls], MCSC_BACKGROUND, MCSC_MONTHBK, MCSC_TEXT, MCSC_TITLEBK, MCSC_TITLETEXT, MCSC_TRAILINGTEXT, _win32_DateTime_SetMonthCalColor, _win32_DateTime_SetMonthCalColor_cpp, commctrl/DateTime_SetMonthCalColor, controls.DateTime_SetMonthCalColor, controls._win32_DateTime_SetMonthCalColor
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	DateTime_SetMonthCalColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DateTime_SetMonthCalColor macro


## -description


Sets the color for a given portion of the month calendar within a date and time picker (DTP) control. You can use this macro or send the <a href="https://msdn.microsoft.com/cee72c1d-58da-4ee5-850e-a615ec6ad079">DTM_SETMCCOLOR</a> message explicitly. 


## -parameters




### -param hdp

TBD


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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>


					A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that represents the color that will be set for the specified area of the month calendar. 


#### - hwndDP

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a DTP control. 


## -remarks



When visual styles are enabled, this macro has no effect except when <i>iColor</i> is MCSC_BACKGROUND.	



