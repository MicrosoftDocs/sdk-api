---
UID: NS:winuser.tagSCROLLBARINFO
title: SCROLLBARINFO (winuser.h)
description: The SCROLLBARINFO structure contains scroll bar information.
helpviewer_keywords: ["*LPSCROLLBARINFO","*PSCROLLBARINFO","LPSCROLLBARINFO","LPSCROLLBARINFO structure pointer [Windows Controls]","PSCROLLBARINFO","PSCROLLBARINFO structure pointer [Windows Controls]","SCROLLBARINFO","SCROLLBARINFO structure [Windows Controls]","STATE_SYSTEM_INVISIBLE","STATE_SYSTEM_OFFSCREEN","STATE_SYSTEM_PRESSED","STATE_SYSTEM_UNAVAILABLE","_win32_SCROLLBARINFO_str","_win32_SCROLLBARINFO_str_cpp","controls.SCROLLBARINFO","controls._win32_SCROLLBARINFO_str","winuser/LPSCROLLBARINFO","winuser/PSCROLLBARINFO","winuser/SCROLLBARINFO"]
old-location: controls\SCROLLBARINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarstructures\scrollbarinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPSCROLLBARINFO, *PSCROLLBARINFO, LPSCROLLBARINFO, LPSCROLLBARINFO structure pointer [Windows Controls], PSCROLLBARINFO, PSCROLLBARINFO structure pointer [Windows Controls], SCROLLBARINFO, SCROLLBARINFO structure [Windows Controls], STATE_SYSTEM_INVISIBLE, STATE_SYSTEM_OFFSCREEN, STATE_SYSTEM_PRESSED, STATE_SYSTEM_UNAVAILABLE, _win32_SCROLLBARINFO_str, _win32_SCROLLBARINFO_str_cpp, controls.SCROLLBARINFO, controls._win32_SCROLLBARINFO_str, winuser/LPSCROLLBARINFO, winuser/PSCROLLBARINFO, winuser/SCROLLBARINFO'
req.header: winuser.h
req.include-header: Windows.h
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
req.typenames: SCROLLBARINFO, *PSCROLLBARINFO, *LPSCROLLBARINFO
req.redist: Service Pack 6
ms.custom: 19H1
f1_keywords:
 - tagSCROLLBARINFO
 - winuser/tagSCROLLBARINFO
 - PSCROLLBARINFO
 - winuser/PSCROLLBARINFO
 - SCROLLBARINFO
 - winuser/SCROLLBARINFO
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
 - SCROLLBARINFO
---

# SCROLLBARINFO structure


## -description

The <b>SCROLLBARINFO</b> structure contains scroll bar information.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the size, in bytes, of the structure. Before calling the <a href="/windows/desktop/api/winuser/nf-winuser-getscrollbarinfo">GetScrollBarInfo</a> function, set <b>cbSize</b> to <b>sizeof</b>(<b>SCROLLBARINFO</b>).

### -field rcScrollBar

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

Coordinates of the scroll bar as specified in a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure.

### -field dxyLineButton

Type: <b>int</b>

Height or width of the thumb.

### -field xyThumbTop

Type: <b>int</b>

Position of the top or left of the thumb.

### -field xyThumbBottom

Type: <b>int</b>

Position of the bottom or right of the thumb.

### -field reserved

Type: <b>int</b>

Reserved.

### -field rgstate

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>[CCHILDREN_SCROLLBAR+1]</b>

An array of <b>DWORD</b> elements. Each element indicates the state of a scroll bar component. The following values show the scroll bar component that corresponds to each array index.
					

<table class="clsStd">
<tr>
<th>Index</th>
<th>Scroll bar component</th>
</tr>
<tr>
<td>0</td>
<td>The scroll bar itself.</td>
</tr>
<tr>
<td>1</td>
<td>The top or right arrow button.</td>
</tr>
<tr>
<td>2</td>
<td>The page up or page right region.</td>
</tr>
<tr>
<td>3</td>
<td>The scroll box (thumb).</td>
</tr>
<tr>
<td>4</td>
<td>The page down or page left region.</td>
</tr>
<tr>
<td>5</td>
<td>The bottom or left arrow button.</td>
</tr>
</table>
 

The <b>DWORD</b> element for each scroll bar component can include a combination of the following bit flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_INVISIBLE"></a><a id="state_system_invisible"></a><dl>
<dt><b>STATE_SYSTEM_INVISIBLE</b></dt>
</dl>
</td>
<td width="60%">
For the scroll bar itself, indicates the specified vertical or horizontal scroll bar does not exist. For the page up or page down regions, indicates the thumb is positioned such that the region does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_OFFSCREEN"></a><a id="state_system_offscreen"></a><dl>
<dt><b>STATE_SYSTEM_OFFSCREEN</b></dt>
</dl>
</td>
<td width="60%">
For the scroll bar itself, indicates the window is sized such that the specified vertical or horizontal scroll bar is not currently displayed.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_PRESSED"></a><a id="state_system_pressed"></a><dl>
<dt><b>STATE_SYSTEM_PRESSED</b></dt>
</dl>
</td>
<td width="60%">
The arrow button or page region is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_UNAVAILABLE"></a><a id="state_system_unavailable"></a><dl>
<dt><b>STATE_SYSTEM_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The component is disabled.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getscrollbarinfo">GetScrollBarInfo</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/scroll-bars">Scroll Bars</a>