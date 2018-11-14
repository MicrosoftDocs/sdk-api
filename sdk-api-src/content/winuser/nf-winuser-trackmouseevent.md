---
UID: NF:winuser.TrackMouseEvent
title: TrackMouseEvent function
author: windows-sdk-content
description: Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.
old-location: inputdev\trackmouseevent.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\trackmouseevent.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: TrackMouseEvent, TrackMouseEvent function [Keyboard and Mouse Input], _win32_TrackMouseEvent, _win32_trackmouseevent_cpp, inputdev.trackmouseevent, winui._win32_trackmouseevent, winuser/TrackMouseEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-mouse-l1-1-0.dll
 - api-ms-win-ntuser-ie-mouse-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - TrackMouseEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- TrackMouseEvent
: 
---

# TrackMouseEvent function


## -description


Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.
<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/en-us/library/ms646266(v=VS.85).aspx">_TrackMouseEvent</a> function calls <b>TrackMouseEvent</b> if it exists, otherwise <b>_TrackMouseEvent</b> emulates <b>TrackMouseEvent</b>. </div><div> </div>

## -parameters




### -param lpEventTrack [in, out]

Type: <b>LPTRACKMOUSEEVENT</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms645604(v=VS.85).aspx">TRACKMOUSEEVENT</a> structure that contains tracking information. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero . 

If the function fails, return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
 




## -remarks



The mouse pointer is considered to be hovering when it stays within a specified rectangle for a specified period of time. Call 
				<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>.
 and use the values <b>SPI_GETMOUSEHOVERWIDTH</b>, <b>SPI_GETMOUSEHOVERHEIGHT</b>, and <b>SPI_GETMOUSEHOVERTIME</b> to retrieve the size of the rectangle and the time.

The function can post the following messages.

<table>
<tr>
<th>Message</th>
<th>Description</th>
</tr>
<tr>
<td><b>WM_NCMOUSEHOVER</b></td>
<td>The same meaning as <a href="https://msdn.microsoft.com/en-us/library/ms645613(v=VS.85).aspx">WM_MOUSEHOVER</a> except this is for the nonclient area of the window.</td>
</tr>
<tr>
<td><b>WM_NCMOUSELEAVE</b></td>
<td>The same meaning as <a href="https://msdn.microsoft.com/en-us/library/ms645615(v=VS.85).aspx">WM_MOUSELEAVE</a> except this is for the nonclient area of the window.</td>
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



<a href="https://msdn.microsoft.com/en-us/library/ms645533(v=VS.85).aspx">Mouse Input</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645604(v=VS.85).aspx">TRACKMOUSEEVENT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646266(v=VS.85).aspx">_TrackMouseEvent</a>
 

 

