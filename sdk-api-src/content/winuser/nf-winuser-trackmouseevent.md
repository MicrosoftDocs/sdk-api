---
UID: NF:winuser.TrackMouseEvent
title: TrackMouseEvent function
author: windows-sdk-content
description: Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.
old-location: inputdev\trackmouseevent.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\trackmouseevent.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: TrackMouseEvent, TrackMouseEvent function [Keyboard and Mouse Input], _win32_TrackMouseEvent, _win32_trackmouseevent_cpp, inputdev.trackmouseevent, winui._win32_trackmouseevent, winuser/TrackMouseEvent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# TrackMouseEvent function


## -description


Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.
<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/8ecdf786-92d2-4035-8e33-dbf32dd8131f">_TrackMouseEvent</a> function calls <b>TrackMouseEvent</b> if it exists, otherwise <b>_TrackMouseEvent</b> emulates <b>TrackMouseEvent</b>. </div><div> </div>

## -parameters




### -param lpEventTrack [in, out]

Type: <b>LPTRACKMOUSEEVENT</b>

A pointer to a <a href="https://msdn.microsoft.com/6c367eeb-5dd4-4a3a-b7d6-9504d2089112">TRACKMOUSEEVENT</a> structure that contains tracking information. 


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
<td>The same meaning as <a href="https://msdn.microsoft.com/efba7f04-2d26-44f1-89df-a565c03ad944">WM_MOUSEHOVER</a> except this is for the nonclient area of the window.</td>
</tr>
<tr>
<td><b>WM_NCMOUSELEAVE</b></td>
<td>The same meaning as <a href="https://msdn.microsoft.com/b23d24ff-531a-4b6d-8848-f82ac5568995">WM_MOUSELEAVE</a> except this is for the nonclient area of the window.</td>
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



<a href="https://msdn.microsoft.com/35f5e1ad-74d5-41bb-9016-b1c5de449550">Mouse Input</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>



<a href="https://msdn.microsoft.com/6c367eeb-5dd4-4a3a-b7d6-9504d2089112">TRACKMOUSEEVENT</a>



<a href="https://msdn.microsoft.com/8ecdf786-92d2-4035-8e33-dbf32dd8131f">_TrackMouseEvent</a>
 

 

