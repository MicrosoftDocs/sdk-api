---
UID: NF:commctrl.MonthCal_SetColor
title: MonthCal_SetColor macro
author: windows-sdk-content
description: Sets the color for a given portion of a month calendar control. You can use this macro or send the MCM_SETCOLOR message explicitly.
old-location: controls\MonthCal_SetColor.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcolor.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MCSC_BACKGROUND, MCSC_MONTHBK, MCSC_TEXT, MCSC_TITLEBK, MCSC_TITLETEXT, MCSC_TRAILINGTEXT, MonthCal_SetColor, MonthCal_SetColor macro [Windows Controls], _win32_MonthCal_SetColor, _win32_MonthCal_SetColor_cpp, commctrl/MonthCal_SetColor, controls.MonthCal_SetColor, controls._win32_MonthCal_SetColor
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
 - MonthCal_SetColor
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
- MonthCal_SetColor
: 
---

# MonthCal_SetColor macro


## -description


Sets the color for a given portion of a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/4ceb7b0e-82be-474a-a163-7e71356818c0">MCM_SETCOLOR</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


### -param iColor

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Value of type <b>int</b> specifying which month calendar color to set. This value can be one of the following: 

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

<b>COLORREF</b> value that represents the color that will be set for the specified area of the month calendar. 


## -remarks



If visual styles are active, this macro has no effect except when <i>iColor</i> is MCSC_BACKGROUND.
            



