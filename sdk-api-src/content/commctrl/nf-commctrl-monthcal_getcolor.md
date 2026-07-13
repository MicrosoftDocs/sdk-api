---
UID: NF:commctrl.MonthCal_GetColor
title: MonthCal_GetColor macro (commctrl.h)
description: Retrieves the color for a given portion of a month calendar control. You can use this macro or send the MCM_GETCOLOR message explicitly.
helpviewer_keywords: ["MCSC_BACKGROUND","MCSC_MONTHBK","MCSC_TEXT","MCSC_TITLEBK","MCSC_TITLETEXT","MCSC_TRAILINGTEXT","MonthCal_GetColor","MonthCal_GetColor macro [Windows Controls]","_win32_MonthCal_GetColor","_win32_MonthCal_GetColor_cpp","commctrl/MonthCal_GetColor","controls.MonthCal_GetColor","controls._win32_MonthCal_GetColor"]
old-location: controls\MonthCal_GetColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getcolor.htm
ms.date: 10/21/2024
ms.keywords: MCSC_BACKGROUND, MCSC_MONTHBK, MCSC_TEXT, MCSC_TITLEBK, MCSC_TITLETEXT, MCSC_TRAILINGTEXT, MonthCal_GetColor, MonthCal_GetColor macro [Windows Controls], _win32_MonthCal_GetColor, _win32_MonthCal_GetColor_cpp, commctrl/MonthCal_GetColor, controls.MonthCal_GetColor, controls._win32_MonthCal_GetColor
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
 - MonthCal_GetColor
 - commctrl/MonthCal_GetColor
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
 - MonthCal_GetColor
---

# MonthCal_GetColor macro

## -syntax

```cpp
COLORREF MonthCal_GetColor(
   HWND hmc,
   INT  iColor
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns a <b>COLORREF</b> value that represents the color setting for the specified portion of the month calendar control if successful. Otherwise, the return is -1.

## -description

Retrieves the color for a given portion of a month calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getcolor">MCM_GETCOLOR</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param iColor

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Value of type <b>int</b> specifying which month calendar color to retrieve. This value can be one of the following: 

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
Retrieve the background color displayed between months.

</td>
</tr>
<tr>
<td width="40%"><a id="MCSC_MONTHBK"></a><a id="mcsc_monthbk"></a><dl>
<dt><b>MCSC_MONTHBK</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the background color displayed within the month.

</td>
</tr>
<tr>
<td width="40%"><a id="MCSC_TEXT"></a><a id="mcsc_text"></a><dl>
<dt><b>MCSC_TEXT</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the color used to display text within a month.

</td>
</tr>
<tr>
<td width="40%"><a id="MCSC_TITLEBK"></a><a id="mcsc_titlebk"></a><dl>
<dt><b>MCSC_TITLEBK</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the background color displayed in the calendar's title.

</td>
</tr>
<tr>
<td width="40%"><a id="MCSC_TITLETEXT"></a><a id="mcsc_titletext"></a><dl>
<dt><b>MCSC_TITLETEXT</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the color used to display text within the calendar's title.

</td>
</tr>
<tr>
<td width="40%"><a id="MCSC_TRAILINGTEXT"></a><a id="mcsc_trailingtext"></a><dl>
<dt><b>MCSC_TRAILINGTEXT</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the color used to display header day and trailing day text. Header and trailing days are the days from the previous and following months that appear on the current month calendar.

</td>
</tr>
</table>
