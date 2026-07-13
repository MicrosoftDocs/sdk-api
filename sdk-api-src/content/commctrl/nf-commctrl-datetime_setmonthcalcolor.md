---
UID: NF:commctrl.DateTime_SetMonthCalColor
title: DateTime_SetMonthCalColor macro (commctrl.h)
description: Sets the color for a given portion of the month calendar within a date and time picker (DTP) control. You can use this macro or send the DTM_SETMCCOLOR message explicitly.
helpviewer_keywords: ["DateTime_SetMonthCalColor","DateTime_SetMonthCalColor macro [Windows Controls]","MCSC_BACKGROUND","MCSC_MONTHBK","MCSC_TEXT","MCSC_TITLEBK","MCSC_TITLETEXT","MCSC_TRAILINGTEXT","_win32_DateTime_SetMonthCalColor","_win32_DateTime_SetMonthCalColor_cpp","commctrl/DateTime_SetMonthCalColor","controls.DateTime_SetMonthCalColor","controls._win32_DateTime_SetMonthCalColor"]
old-location: controls\DateTime_SetMonthCalColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setmonthcalcolor.htm
ms.date: 10/21/2024
ms.keywords: DateTime_SetMonthCalColor, DateTime_SetMonthCalColor macro [Windows Controls], MCSC_BACKGROUND, MCSC_MONTHBK, MCSC_TEXT, MCSC_TITLEBK, MCSC_TITLETEXT, MCSC_TRAILINGTEXT, _win32_DateTime_SetMonthCalColor, _win32_DateTime_SetMonthCalColor_cpp, commctrl/DateTime_SetMonthCalColor, controls.DateTime_SetMonthCalColor, controls._win32_DateTime_SetMonthCalColor
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
 - DateTime_SetMonthCalColor
 - commctrl/DateTime_SetMonthCalColor
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
 - DateTime_SetMonthCalColor
---

# DateTime_SetMonthCalColor macro

## -syntax

```cpp
COLORREF DateTime_SetMonthCalColor(
   HWND     hdp,
   int      iColor,
   COLORREF clr
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns a <b>COLORREF</b> value that represents the previous color setting for the specified portion of the month calendar control if successful. Otherwise, this message returns -1.

## -description

Sets the color for a given portion of the month calendar within a date and time picker (DTP) control. You can use this macro or send the <a href="/windows/desktop/Controls/dtm-setmccolor">DTM_SETMCCOLOR</a> message explicitly.

## -parameters

### -param hdp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

A <a href="/windows/desktop/gdi/colorref">COLORREF</a> value that represents the color that will be set for the specified area of the month calendar.

## -remarks

When visual styles are enabled, this macro has no effect except when <i>iColor</i> is MCSC_BACKGROUND.
