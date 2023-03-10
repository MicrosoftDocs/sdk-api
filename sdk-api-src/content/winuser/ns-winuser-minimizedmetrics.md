---
UID: NS:winuser.tagMINIMIZEDMETRICS
title: MINIMIZEDMETRICS (winuser.h)
description: Contains the scalable metrics associated with minimized windows.
helpviewer_keywords: ["*LPMINIMIZEDMETRICS","*PMINIMIZEDMETRICS","ARW_BOTTOMLEFT","ARW_BOTTOMRIGHT","ARW_DOWN","ARW_HIDE","ARW_LEFT","ARW_RIGHT","ARW_TOPLEFT","ARW_TOPRIGHT","ARW_UP","LPMINIMIZEDMETRICS","LPMINIMIZEDMETRICS structure pointer [Windows and Messages]","MINIMIZEDMETRICS","MINIMIZEDMETRICS structure [Windows and Messages]","PMINIMIZEDMETRICS","PMINIMIZEDMETRICS structure pointer [Windows and Messages]","_win32_minimizedmetrics_str","base.minimizedmetrics_str","minimizedmetrics_str_cpp","tagMINIMIZEDMETRICS","winmsg.minimizedmetrics_str","winui.minimizedmetrics_str","winuser/LPMINIMIZEDMETRICS","winuser/MINIMIZEDMETRICS","winuser/PMINIMIZEDMETRICS"]
old-location: winmsg\minimizedmetrics_str.htm
tech.root: winmsg
ms.assetid: 10ae6579-2d66-4e8f-8692-0be8abdbf41a
ms.date: 12/05/2018
ms.keywords: '*LPMINIMIZEDMETRICS, *PMINIMIZEDMETRICS, ARW_BOTTOMLEFT, ARW_BOTTOMRIGHT, ARW_DOWN, ARW_HIDE, ARW_LEFT, ARW_RIGHT, ARW_TOPLEFT, ARW_TOPRIGHT, ARW_UP, LPMINIMIZEDMETRICS, LPMINIMIZEDMETRICS structure pointer [Windows and Messages], MINIMIZEDMETRICS, MINIMIZEDMETRICS structure [Windows and Messages], PMINIMIZEDMETRICS, PMINIMIZEDMETRICS structure pointer [Windows and Messages], _win32_minimizedmetrics_str, base.minimizedmetrics_str, minimizedmetrics_str_cpp, tagMINIMIZEDMETRICS, winmsg.minimizedmetrics_str, winui.minimizedmetrics_str, winuser/LPMINIMIZEDMETRICS, winuser/MINIMIZEDMETRICS, winuser/PMINIMIZEDMETRICS'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MINIMIZEDMETRICS, *PMINIMIZEDMETRICS, *LPMINIMIZEDMETRICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMINIMIZEDMETRICS
 - winuser/tagMINIMIZEDMETRICS
 - PMINIMIZEDMETRICS
 - winuser/PMINIMIZEDMETRICS
 - MINIMIZEDMETRICS
 - winuser/MINIMIZEDMETRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MINIMIZEDMETRICS
---

# MINIMIZEDMETRICS structure


## -description

Contains the scalable metrics associated with minimized windows. This structure is used with the 
<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function when the SPI_GETMINIMIZEDMETRICS or SPI_SETMINIMIZEDMETRICS action value is specified.

## -struct-fields

### -field cbSize

The size of the structure, in bytes. The caller must set this to <code>sizeof(MINIMIZEDMETRICS)</code>.

### -field iWidth

The width of minimized windows, in pixels.

### -field iHorzGap

The horizontal space between arranged minimized windows, in pixels.

### -field iVertGap

The vertical space between arranged minimized windows, in pixels.

### -field iArrange

The starting position and direction used when arranging minimized windows. The starting position must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ARW_BOTTOMLEFT"></a><a id="arw_bottomleft"></a><dl>
<dt><b>ARW_BOTTOMLEFT</b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
Start at the lower-left corner of the work area.

</td>
</tr>
<tr>
<td width="40%"><a id="ARW_BOTTOMRIGHT"></a><a id="arw_bottomright"></a><dl>
<dt><b>ARW_BOTTOMRIGHT</b></dt>
<dt>0x0001L</dt>
</dl>
</td>
<td width="60%">
Start at the lower-right corner of the work area.

</td>
</tr>
<tr>
<td width="40%"><a id="ARW_TOPLEFT"></a><a id="arw_topleft"></a><dl>
<dt><b>ARW_TOPLEFT</b></dt>
<dt>0x0002L</dt>
</dl>
</td>
<td width="60%">
Start at the upper-left corner of the work area.

</td>
</tr>
<tr>
<td width="40%"><a id="ARW_TOPRIGHT"></a><a id="arw_topright"></a><dl>
<dt><b>ARW_TOPRIGHT</b></dt>
<dt>0x0003L</dt>
</dl>
</td>
<td width="60%">
Start at the upper-right corner of the work area.

</td>
</tr>
</table>
 

The direction must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ARW_LEFT"></a><a id="arw_left"></a><dl>
<dt><b>ARW_LEFT</b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
Arrange left (valid with ARW_BOTTOMRIGHT and ARW_TOPRIGHT only).

</td>
</tr>
<tr>
<td width="40%"><a id="ARW_RIGHT"></a><a id="arw_right"></a><dl>
<dt><b>ARW_RIGHT</b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
Arrange right (valid with ARW_BOTTOMLEFT and ARW_TOPLEFT only).

</td>
</tr>
<tr>
<td width="40%"><a id="ARW_UP"></a><a id="arw_up"></a><dl>
<dt><b>ARW_UP</b></dt>
<dt>0x0004L</dt>
</dl>
</td>
<td width="60%">
Arrange up (valid with ARW_BOTTOMLEFT and ARW_BOTTOMRIGHT only).

</td>
</tr>
<tr>
<td width="40%"><a id="ARW_DOWN"></a><a id="arw_down"></a><dl>
<dt><b>ARW_DOWN</b></dt>
<dt>0x0004L</dt>
</dl>
</td>
<td width="60%">
Arrange down (valid with ARW_TOPLEFT and ARW_TOPRIGHT only).

</td>
</tr>
<tr>
<td width="40%"><a id="ARW_HIDE"></a><a id="arw_hide"></a><dl>
<dt><b>ARW_HIDE</b></dt>
<dt>0x0008L</dt>
</dl>
</td>
<td width="60%">
Hide minimized windows by moving them off the visible area of the screen.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>