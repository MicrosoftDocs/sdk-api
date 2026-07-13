---
UID: NF:winuser.GetQueueStatus
title: GetQueueStatus function (winuser.h)
description: Retrieves the type of messages found in the calling thread's message queue.
helpviewer_keywords: ["GetQueueStatus","GetQueueStatus function [Windows and Messages]","QS_ALLEVENTS","QS_ALLINPUT","QS_ALLPOSTMESSAGE","QS_HOTKEY","QS_INPUT","QS_KEY","QS_MOUSE","QS_MOUSEBUTTON","QS_MOUSEMOVE","QS_PAINT","QS_POSTMESSAGE","QS_RAWINPUT","QS_SENDMESSAGE","QS_TIMER","_win32_GetQueueStatus","_win32_getqueuestatus_cpp","winmsg.getqueuestatus","winui._win32_getqueuestatus","winuser/GetQueueStatus"]
old-location: winmsg\getqueuestatus.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getqueuestatus.htm
ms.date: 12/05/2018
ms.keywords: GetQueueStatus, GetQueueStatus function [Windows and Messages], QS_ALLEVENTS, QS_ALLINPUT, QS_ALLPOSTMESSAGE, QS_HOTKEY, QS_INPUT, QS_KEY, QS_MOUSE, QS_MOUSEBUTTON, QS_MOUSEMOVE, QS_PAINT, QS_POSTMESSAGE, QS_RAWINPUT, QS_SENDMESSAGE, QS_TIMER, _win32_GetQueueStatus, _win32_getqueuestatus_cpp, winmsg.getqueuestatus, winui._win32_getqueuestatus, winuser/GetQueueStatus
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
 - GetQueueStatus
 - winuser/GetQueueStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
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
 - GetQueueStatus
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# GetQueueStatus function


## -description

Retrieves the type of messages found in the calling thread's message queue.

## -parameters

### -param flags [in]

Type: <b>UINT</b>

The types of messages for which to check. This parameter can be one or more of the following values.

| Value | Meaning |
|-------|---------|
| **QS\_KEY**<br>0x0001 | A [WM\_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM\_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM\_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup), or [WM\_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown) message is in the queue. |
| **QS\_MOUSEMOVE**<br>0x0002 | A [WM\_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove) message is in the queue. |
| **QS\_MOUSEBUTTON**<br>0x0004 | A mouse-button message ([WM\_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM\_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown), and so on). |
| **QS\_POSTMESSAGE**<br>0x0008 | A posted message (other than those listed here) is in the queue. For more information, see [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagew).<br>This value is cleared when you call [GetMessage](/windows/win32/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagew), whether or not you are filtering messages. |
| **QS\_TIMER**<br>0x0010 | A [WM\_TIMER](/windows/desktop/winmsg/wm-timer) message is in the queue. |
| **QS\_PAINT**<br>0x0020 | A [WM\_PAINT](/windows/desktop/gdi/wm-paint) message is in the queue. |
| **QS\_SENDMESSAGE**<br>0x0040 | A message sent by another thread or application is in the queue. For more information, see [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessagew). |
| **QS\_HOTKEY**<br>0x0080 | A [WM\_HOTKEY](/windows/desktop/inputdev/wm-hotkey) message is in the queue. |
| **QS\_ALLPOSTMESSAGE**<br>0x0100 | A posted message (other than those listed here) is in the queue. For more information, see [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagew).<br>This value is cleared when you call GetMessage or PeekMessage without filtering messages. | 
| **QS\_RAWINPUT**<br>0x0400 | Windows XP and newer: A raw input message is in the queue. For more information, see [Raw Input](/windows/desktop/inputdev/raw-input). |
| **QS\_TOUCH**<br>0x0800 | Windows 8 and newer: A touch input message is in the queue. For more information, see [Touch Input](/windows/win32/wintouch/windows-touch-portal). |
| **QS\_POINTER**<br>0x1000 | Windows 8 and newer: A pointer input message is in the queue. For more information, see [Pointer Input](/windows/win32/inputmsg/messages-and-notifications-portal). |
| **QS\_MOUSE**<br>(QS\_MOUSEMOVE \| QS\_MOUSEBUTTON) | A [WM\_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove) message or mouse-button message ([WM\_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM\_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown), and so on). |
| **QS\_INPUT**<br>(QS\_MOUSE \| QS\_KEY \| QS\_RAWINPUT \| QS\_TOUCH \| QS\_POINTER) | An input message is in the queue. |
| **QS\_ALLEVENTS**<br>(QS\_INPUT \| QS\_POSTMESSAGE \| QS\_TIMER \| QS\_PAINT \| QS\_HOTKEY) | An input, [WM\_TIMER](/windows/desktop/winmsg/wm-timer), [WM\_PAINT](/windows/desktop/gdi/wm-paint), [WM\_HOTKEY](/windows/desktop/inputdev/wm-hotkey), or posted message is in the queue. |
| **QS\_ALLINPUT**<br>(QS\_INPUT \| QS\_POSTMESSAGE \| QS\_TIMER \| QS\_PAINT \| QS\_HOTKEY \| QS\_SENDMESSAGE) | Any message is in the queue. |


## -returns

Type: <b>DWORD</b>

The high-order word of the return value indicates the types of messages currently in the queue. The low-order word indicates the types of messages that have been added to the queue and that are still in the queue since the last call to the <b>GetQueueStatus</b>, <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>, or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> function.

## -remarks

The presence of a QS_ flag in the return value does not guarantee that a subsequent call to the <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> function will return a message. <b>GetMessage</b> and <b>PeekMessage</b> perform some internal filtering that may cause the message to be processed internally. For this reason, the return value from <b>GetQueueStatus</b> should be considered only a hint as to whether <b>GetMessage</b> or <b>PeekMessage</b> should be called. 

The <b>QS_ALLPOSTMESSAGE</b> and <b>QS_POSTMESSAGE</b> flags differ in when they are cleared. <b>QS_POSTMESSAGE</b> is cleared when you call <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>, whether or not you are filtering messages. <b>QS_ALLPOSTMESSAGE</b> is cleared when you call <b>GetMessage</b> or <b>PeekMessage</b> without filtering messages (<i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> are 0). This can be useful when you call <b>PeekMessage</b> multiple times to get messages in different ranges.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getinputstate">GetInputState</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<b>Reference</b>
