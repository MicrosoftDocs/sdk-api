---
UID: NF:scrnsave.DefScreenSaverProc
title: DefScreenSaverProc function
author: windows-sdk-content
description: Provides default processing for any messages that a screen saver application does not process.
old-location: shell\DefScreenSaverProc.htm
old-project: shell
ms.assetid: eda5c4d4-0484-4c81-a699-5fedea0bd1c2
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: DefScreenSaverProc, DefScreenSaverProc function [Windows Shell], _win32_DefScreenSaverProc, scrnsave/DefScreenSaverProc, shell.DefScreenSaverProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: scrnsave.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: SCHEDULE_HEADER, *PSCHEDULE_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - None
api_name:
 - DefScreenSaverProc
product: Windows
targetos: Windows
req.lib: Scrnsave.lib
req.dll: None
req.irql: 
req.product: ADAM
---

# DefScreenSaverProc function


## -description


Provides default processing for any messages that a screen saver application does not process.


## -parameters




### -param hWnd

Type: <b>HWND</b>

The identifier of the screen saver window.


### -param msg

Type: <b>UINT</b>

The message to be processed. The <b>DefScreenSaverProc</b> function responds to messages that affect the screen saver's operation, as detailed in the Remarks section.

If a screen saver application must perform a different action in response to any of these messages, the application's <a href="https://msdn.microsoft.com/cc013841-41fc-404a-a239-4118f70542b5">ScreenSaverProc</a> window procedure should process the message.


### -param wParam

Type: <b>WPARAM</b>

Additional message-specific information.


### -param lParam

Type: <b>LPARAM</b>

Additional message-specific information.


## -returns



Type: <b>LONG</b>

The return value specifies the result of the message processing and depends on the message sent.




## -remarks



A screen saver application's <a href="https://msdn.microsoft.com/cc013841-41fc-404a-a239-4118f70542b5">ScreenSaverProc</a> window procedure should use <b>DefScreenSaverProc</b> instead of the <a href="https://msdn.microsoft.com/library/ms633572(v=VS.85).aspx">DefWindowProc</a> function to provide default message processing. The <b>DefScreenSaverProc</b> function passes any messages that do not affect screen saver operation to <b>DefWindowProc</b>.

The following table describes how the <b>DefScreenSaverProc</b> processes a variety of window messages.

<table class="clsStd">
<tr>
<th>Message</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms646274(v=VS.85).aspx">WM_ACTIVATE</a>, <a href="https://msdn.microsoft.com/library/ms632614(v=VS.85).aspx">WM_ACTIVATEAPP</a>, <a href="https://msdn.microsoft.com/library/ms632633(v=VS.85).aspx">WM_NCACTIVATE</a>
</td>
<td>Closes the screen saver if the <i>wParam</i> parameter is <b>FALSE</b>. A <i>wParam</i> value of <b>FALSE</b> indicates that the screen saver is losing the input focus. The screen saver is closed by sending a <a href="https://msdn.microsoft.com/library/ms632617(v=VS.85).aspx">WM_CLOSE</a> message.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms648382(v=VS.85).aspx">WM_SETCURSOR</a>
</td>
<td>Removes the cursor from the screen by setting the cursor to <b>NULL</b>.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms645607(v=VS.85).aspx">WM_LBUTTONDOWN</a>, <a href="https://msdn.microsoft.com/library/ms646242(v=VS.85).aspx">WM_RBUTTONDOWN</a>, <a href="https://msdn.microsoft.com/library/ms645610(v=VS.85).aspx">WM_MBUTTONDOWN</a>, <a href="https://msdn.microsoft.com/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>, <a href="https://msdn.microsoft.com/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>, <a href="https://msdn.microsoft.com/library/ms645616(v=VS.85).aspx">WM_MOUSEMOVE</a>
</td>
<td>Calls the <a href="https://msdn.microsoft.com/library/ms644945(v=VS.85).aspx">PostQuitMessage</a> function to close the screen saver.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms632620(v=VS.85).aspx">WM_DESTROY</a>
</td>
<td>Posts a <a href="https://msdn.microsoft.com/library/ms632617(v=VS.85).aspx">WM_CLOSE</a> message to close the screen saver window.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms646360(v=VS.85).aspx">WM_SYSCOMMAND</a>
</td>
<td>Returns <b>FALSE</b> if the <i>wParam</i> parameter of <a href="https://msdn.microsoft.com/library/ms646360(v=VS.85).aspx">WM_SYSCOMMAND</a> is either <b>SC_CLOSE</b> or <b>SC_SCREENSAVE</b>.</td>
</tr>
</table>
 



