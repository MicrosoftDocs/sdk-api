---
UID: NF:winuser.PostQuitMessage
title: PostQuitMessage function (winuser.h)
description: Indicates to the system that a thread has made a request to terminate (quit). It is typically used in response to a WM_DESTROY message.
helpviewer_keywords: ["PostQuitMessage","PostQuitMessage function [Windows and Messages]","_win32_PostQuitMessage","_win32_postquitmessage_cpp","winmsg.postquitmessage","winui._win32_postquitmessage","winuser/PostQuitMessage"]
old-location: winmsg\postquitmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\postquitmessage.htm
ms.date: 12/05/2018
ms.keywords: PostQuitMessage, PostQuitMessage function [Windows and Messages], _win32_PostQuitMessage, _win32_postquitmessage_cpp, winmsg.postquitmessage, winui._win32_postquitmessage, winuser/PostQuitMessage
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
 - PostQuitMessage
 - winuser/PostQuitMessage
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
 - Ext-MS-Win-NTUser-message-l1-1-0.dll
 - Ext-MS-Win-NTUser-message-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - PostQuitMessage
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# PostQuitMessage function


## -description

Indicates to the system that a thread has made a request to terminate (quit). It is typically used in response to a <a href="/windows/desktop/winmsg/wm-destroy">WM_DESTROY</a> message.

## -parameters

### -param nExitCode [in]

Type: <b>int</b>

The application exit code. This value is used as the <i>wParam</i> parameter of the <a href="/windows/desktop/winmsg/wm-quit">WM_QUIT</a> message.

## -remarks

The <b>PostQuitMessage</b> function posts a <a href="/windows/desktop/winmsg/wm-quit">WM_QUIT</a> message to the thread's message queue and returns immediately; the function simply indicates to the system that the thread is requesting to quit at some time in the future. 

When the thread retrieves the <a href="/windows/desktop/winmsg/wm-quit">WM_QUIT</a> message from its message queue, it should exit its message loop and return control to the system. The exit value returned to the system must be the <i>wParam</i> parameter of the <b>WM_QUIT</b> message. 


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-messages-and-message-queues">Posting a Message</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-destroy">WM_DESTROY</a>



<a href="/windows/desktop/winmsg/wm-quit">WM_QUIT</a>
