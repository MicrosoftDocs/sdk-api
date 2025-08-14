---
UID: NF:winuser.TrackMouseEvent
title: TrackMouseEvent function (winuser.h)
description: Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.
helpviewer_keywords: ["TrackMouseEvent","TrackMouseEvent function [Keyboard and Mouse Input]","_win32_TrackMouseEvent","_win32_trackmouseevent_cpp","inputdev.trackmouseevent","winui._win32_trackmouseevent","winuser/TrackMouseEvent"]
old-location: inputdev\trackmouseevent.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\trackmouseevent.htm
ms.date: 12/05/2018
ms.keywords: TrackMouseEvent, TrackMouseEvent function [Keyboard and Mouse Input], _win32_TrackMouseEvent, _win32_trackmouseevent_cpp, inputdev.trackmouseevent, winui._win32_trackmouseevent, winuser/TrackMouseEvent
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TrackMouseEvent
 - winuser/TrackMouseEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-mouse-l1-1-0.dll
 - ext-ms-win-ntuser-mouse-l1-1-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-mouse-l1-1-0.dll
 - api-ms-win-ntuser-ie-mouse-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - TrackMouseEvent
req.apiset: ext-ms-win-ntuser-mouse-l1-1-0 (introduced in Windows 8)
---

# TrackMouseEvent function


## -description

Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.
<div class="alert"><b>Note</b>  The <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent">_TrackMouseEvent</a> function calls <b>TrackMouseEvent</b> if it exists, otherwise <b>_TrackMouseEvent</b> emulates <b>TrackMouseEvent</b>. </div><div> </div>

## -parameters

### -param lpEventTrack [in, out]

Type: <b>LPTRACKMOUSEEVENT</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-trackmouseevent">TRACKMOUSEEVENT</a> structure that contains tracking information.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero . 

If the function fails, return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The mouse pointer is considered to be hovering when it stays within a specified rectangle for a specified period of time. Call 
				<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>.
 and use the values <b>SPI_GETMOUSEHOVERWIDTH</b>, <b>SPI_GETMOUSEHOVERHEIGHT</b>, and <b>SPI_GETMOUSEHOVERTIME</b> to retrieve the size of the rectangle and the time.

The function can post the following messages.

<table>
<tr>
<th>Message</th>
<th>Description</th>
</tr>
<tr>
<td><b>WM_NCMOUSEHOVER</b></td>
<td>The same meaning as <a href="/windows/desktop/inputdev/wm-mousehover">WM_MOUSEHOVER</a> except this is for the nonclient area of the window.</td>
</tr>
<tr>
<td><b>WM_NCMOUSELEAVE</b></td>
<td>The same meaning as <a href="/windows/desktop/inputdev/wm-mouseleave">WM_MOUSELEAVE</a> except this is for the nonclient area of the window.</td>
</tr>
<tr>
<td><b>WM_MOUSEHOVER</b></td>
<td>The mouse hovered over the client area of the window for the period of time specified in a prior call to <b>TrackMouseEvent</b>. Hover tracking stops when this message is generated. The application must call <b>TrackMouseEvent</b> again if it requires further tracking of mouse hover behavior.</td>
</tr>
<tr>
<td><b>WM_MOUSELEAVE</b></td>
<td>The mouse left the client area of the window specified in a prior call to <b>TrackMouseEvent</b>. All tracking requested by <b>TrackMouseEvent</b> is canceled when this message is generated. The application must call <b>TrackMouseEvent</b> when the mouse reenters its window if it requires further tracking of mouse hover behavior.</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>



<a href="/windows/desktop/api/winuser/ns-winuser-trackmouseevent">TRACKMOUSEEVENT</a>



<a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent">_TrackMouseEvent</a>
