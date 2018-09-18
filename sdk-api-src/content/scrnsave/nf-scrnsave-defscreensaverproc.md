---
UID: NF:scrnsave.DefScreenSaverProc
title: DefScreenSaverProc function
author: windows-sdk-content
description: Provides default processing for any messages that a screen saver application does not process.
old-location: shell\DefScreenSaverProc.htm
tech.root: shell
ms.assetid: eda5c4d4-0484-4c81-a699-5fedea0bd1c2
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: DefScreenSaverProc, DefScreenSaverProc function [Windows Shell], _win32_DefScreenSaverProc, scrnsave/DefScreenSaverProc, shell.DefScreenSaverProc
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Scrnsave.lib
req.dll: None
req.irql: 
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
req.typenames: 
req.redist: 
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



A screen saver application's <a href="https://msdn.microsoft.com/cc013841-41fc-404a-a239-4118f70542b5">ScreenSaverProc</a> window procedure should use <b>DefScreenSaverProc</b> instead of the <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> function to provide default message processing. The <b>DefScreenSaverProc</b> function passes any messages that do not affect screen saver operation to <b>DefWindowProc</b>.

The following table describes how the <b>DefScreenSaverProc</b> processes a variety of window messages.

<table class="clsStd">
<tr>
<th>Message</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a62bb9f7-f286-4d0d-a1ca-370950c188b2">WM_ACTIVATE</a>, <a href="https://msdn.microsoft.com/fc3626ac-8f19-4aa6-8fe9-5020d00c09db">WM_ACTIVATEAPP</a>, <a href="https://msdn.microsoft.com/d25732b9-b9ab-4754-a4cf-002d32e3945e">WM_NCACTIVATE</a>
</td>
<td>Closes the screen saver if the <i>wParam</i> parameter is <b>FALSE</b>. A <i>wParam</i> value of <b>FALSE</b> indicates that the screen saver is losing the input focus. The screen saver is closed by sending a <a href="https://msdn.microsoft.com/19500baf-e0ad-4dfa-804f-6a6e0652cffb">WM_CLOSE</a> message.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b722689e-925f-40ac-ba4a-55be9dc6a8f8">WM_SETCURSOR</a>
</td>
<td>Removes the cursor from the screen by setting the cursor to <b>NULL</b>.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2e43720a-98e6-407a-9430-34c288c3da51">WM_LBUTTONDOWN</a>, <a href="https://msdn.microsoft.com/da1a7d7c-6e49-4097-8b43-dcee7bd5fb3f">WM_RBUTTONDOWN</a>, <a href="https://msdn.microsoft.com/5181a425-2577-4806-8926-1075a1a756ee">WM_MBUTTONDOWN</a>, <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>, <a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a>, <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a>
</td>
<td>Calls the <a href="https://msdn.microsoft.com/8abc09a0-d53a-44ff-a91b-ee602260763c">PostQuitMessage</a> function to close the screen saver.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/089c0645-199b-4a90-9cbc-740f0cf3267d">WM_DESTROY</a>
</td>
<td>Posts a <a href="https://msdn.microsoft.com/19500baf-e0ad-4dfa-804f-6a6e0652cffb">WM_CLOSE</a> message to close the screen saver window.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a>
</td>
<td>Returns <b>FALSE</b> if the <i>wParam</i> parameter of <a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a> is either <b>SC_CLOSE</b> or <b>SC_SCREENSAVE</b>.</td>
</tr>
</table>
 



