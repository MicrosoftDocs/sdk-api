---
UID: NF:scrnsave.DefScreenSaverProc
title: DefScreenSaverProc function (scrnsave.h)
description: Provides default processing for any messages that a screen saver application does not process.
helpviewer_keywords: ["DefScreenSaverProc","DefScreenSaverProc function [Windows Shell]","_win32_DefScreenSaverProc","scrnsave/DefScreenSaverProc","shell.DefScreenSaverProc"]
old-location: shell\DefScreenSaverProc.htm
tech.root: shell
ms.assetid: eda5c4d4-0484-4c81-a699-5fedea0bd1c2
ms.date: 12/05/2018
ms.keywords: DefScreenSaverProc, DefScreenSaverProc function [Windows Shell], _win32_DefScreenSaverProc, scrnsave/DefScreenSaverProc, shell.DefScreenSaverProc
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
req.lib: Scrnsave.lib
req.dll: None
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DefScreenSaverProc
 - scrnsave/DefScreenSaverProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - None
api_name:
 - DefScreenSaverProc
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

If a screen saver application must perform a different action in response to any of these messages, the application's <a href="/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc">ScreenSaverProc</a> window procedure should process the message.

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

A screen saver application's <a href="/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc">ScreenSaverProc</a> window procedure should use <b>DefScreenSaverProc</b> instead of the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function to provide default message processing. The <b>DefScreenSaverProc</b> function passes any messages that do not affect screen saver operation to <b>DefWindowProc</b>.

The following table describes how the <b>DefScreenSaverProc</b> processes a variety of window messages.

<table class="clsStd">
<tr>
<th>Message</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/inputdev/wm-activate">WM_ACTIVATE</a>, <a href="/windows/desktop/winmsg/wm-activateapp">WM_ACTIVATEAPP</a>, <a href="/windows/desktop/winmsg/wm-ncactivate">WM_NCACTIVATE</a>
</td>
<td>Closes the screen saver if the <i>wParam</i> parameter is <b>FALSE</b>. A <i>wParam</i> value of <b>FALSE</b> indicates that the screen saver is losing the input focus. The screen saver is closed by sending a <a href="/windows/desktop/winmsg/wm-close">WM_CLOSE</a> message.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/menurc/wm-setcursor">WM_SETCURSOR</a>
</td>
<td>Removes the cursor from the screen by setting the cursor to <b>NULL</b>.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/inputdev/wm-lbuttondown">WM_LBUTTONDOWN</a>, <a href="/windows/desktop/inputdev/wm-rbuttondown">WM_RBUTTONDOWN</a>, <a href="/windows/desktop/inputdev/wm-mbuttondown">WM_MBUTTONDOWN</a>, <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>, <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>, <a href="/windows/desktop/inputdev/wm-mousemove">WM_MOUSEMOVE</a>
</td>
<td>Calls the <a href="/windows/desktop/api/winuser/nf-winuser-postquitmessage">PostQuitMessage</a> function to close the screen saver.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/winmsg/wm-destroy">WM_DESTROY</a>
</td>
<td>Posts a <a href="/windows/desktop/winmsg/wm-close">WM_CLOSE</a> message to close the screen saver window.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a>
</td>
<td>Returns <b>FALSE</b> if the <i>wParam</i> parameter of <a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a> is either <b>SC_CLOSE</b> or <b>SC_SCREENSAVE</b>.</td>
</tr>
</table>