---
UID: NF:winuser.GetMessagePos
title: GetMessagePos function (winuser.h)
description: Retrieves the cursor position for the last message retrieved by the GetMessage function.
helpviewer_keywords: ["GetMessagePos","GetMessagePos function [Windows and Messages]","_win32_GetMessagePos","_win32_getmessagepos_cpp","winmsg.getmessagepos","winui._win32_getmessagepos","winuser/GetMessagePos"]
old-location: winmsg\getmessagepos.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getmessagepos.htm
ms.date: 12/05/2018
ms.keywords: GetMessagePos, GetMessagePos function [Windows and Messages], _win32_GetMessagePos, _win32_getmessagepos_cpp, winmsg.getmessagepos, winui._win32_getmessagepos, winuser/GetMessagePos
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
 - GetMessagePos
 - winuser/GetMessagePos
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-rtcore-ntuser-message-l1-1-0.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-message-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-message-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - GetMessagePos
req.apiset: ext-ms-win-ntuser-message-l1-1-1 (introduced in Windows 8.1)
---

# GetMessagePos function


## -description

Retrieves the cursor position for the last message retrieved by the <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> function.

			

To determine the current position of the cursor, use the <a href="/windows/desktop/api/winuser/nf-winuser-getcursorpos">GetCursorPos</a> function.



## -returns

Type: <b>DWORD</b>

The return value specifies the x- and y-coordinates of the cursor position. The x-coordinate is the low order <b>short</b> and the y-coordinate is the high-order <b>short</b>.

## -remarks

As noted above, the x-coordinate is in the low-order <b>short</b> of the return value; the y-coordinate is in the high-order <b>short</b> (both represent <i>signed</i> values because they can take negative values on systems with multiple monitors). If the return value is assigned to a variable, you can use the <a href="/windows/desktop/api/wingdi/nf-wingdi-makepoints">MAKEPOINTS</a> macro to obtain a <a href="/windows/win32/api/windef/ns-windef-points">POINTS</a> structure from the return value. You can also use the <a href="/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam">GET_X_LPARAM</a> or <a href="/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam">GET_Y_LPARAM</a> macro to extract the x- or y-coordinate. 

<div class="alert"><b>Important</b>  Do not use the <a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> or <a href="/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)">HIWORD</a> macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors. Systems with multiple monitors can have negative x- and y- coordinates, and <b>LOWORD</b> and <b>HIWORD</b> treat the coordinates as unsigned quantities.</div>
<div> </div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getcursorpos">GetCursorPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessagetime">GetMessageTime</a>



<a href="/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)">HIWORD</a>



<a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-makepoints">MAKEPOINTS</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<b>Other Resources</b>



<a href="/windows/win32/api/windef/ns-windef-points">POINTS</a>



<b>Reference</b>
