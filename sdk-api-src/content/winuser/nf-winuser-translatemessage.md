---
UID: NF:winuser.TranslateMessage
title: TranslateMessage function (winuser.h)
description: Translates virtual-key messages into character messages. The character messages are posted to the calling thread's message queue, to be read the next time the thread calls the GetMessage or PeekMessage function.
helpviewer_keywords: ["TranslateMessage","TranslateMessage function [Windows and Messages]","_win32_TranslateMessage","_win32_translatemessage_cpp","winmsg.translatemessage","winui._win32_translatemessage","winuser/TranslateMessage"]
old-location: winmsg\translatemessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\translatemessage.htm
ms.date: 12/05/2018
ms.keywords: TranslateMessage, TranslateMessage function [Windows and Messages], _win32_TranslateMessage, _win32_translatemessage_cpp, winmsg.translatemessage, winui._win32_translatemessage, winuser/TranslateMessage
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
 - TranslateMessage
 - winuser/TranslateMessage
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
 - TranslateMessage
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# TranslateMessage function


## -description

Translates virtual-key messages into character messages. The character messages are posted to the calling thread's message queue, to be read the next time the thread calls the <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> function.

## -parameters

### -param lpMsg [in]

Type: <b>const <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>*</b>

A pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that contains message information retrieved from the calling thread's message queue by using the <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> function.

## -returns

Type: <b>BOOL</b>

If the message is translated (that is, a character message is posted to the thread's message queue), the return value is nonzero.

If the message is <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>, <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>, <a href="/windows/desktop/inputdev/wm-syskeydown">WM_SYSKEYDOWN</a>, or <a href="/windows/desktop/inputdev/wm-syskeyup">WM_SYSKEYUP</a>, the return value is nonzero, regardless of the translation. 

If the message is not translated (that is, a character message is not posted to the thread's message queue), the return value is zero.

## -remarks

The <b>TranslateMessage</b> function does not modify the message pointed to by the <i>lpMsg</i> parameter. 


<a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a> and <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a> combinations produce a <a href="/windows/desktop/inputdev/wm-char">WM_CHAR</a> or <a href="/windows/desktop/inputdev/wm-deadchar">WM_DEADCHAR</a> message. <a href="/windows/desktop/inputdev/wm-syskeydown">WM_SYSKEYDOWN</a> and <a href="/windows/desktop/inputdev/wm-syskeyup">WM_SYSKEYUP</a> combinations produce a <a href="/windows/desktop/menurc/wm-syschar">WM_SYSCHAR</a> or <a href="/windows/desktop/inputdev/wm-sysdeadchar">WM_SYSDEADCHAR</a> message. 

<b>TranslateMessage</b> produces <a href="/windows/desktop/inputdev/wm-char">WM_CHAR</a> messages only for keys that are mapped to ASCII characters by the keyboard driver. 

If applications process virtual-key messages for some other purpose, they should not call <b>TranslateMessage</b>. For instance, an application should not call <b>TranslateMessage</b> if the <a href="/windows/desktop/api/winuser/nf-winuser-translateacceleratora">TranslateAccelerator</a> function returns a nonzero value. Note that the application is responsible for retrieving and dispatching input messages to the dialog box. Most applications use the main message loop for this. However, to permit the user to move to and to select controls by using the keyboard, the application must call <a href="/windows/desktop/api/winuser/nf-winuser-isdialogmessagea">IsDialogMessage</a>. For more information, see  <a href="/windows/desktop/dlgbox/dlgbox-programming-considerations">Dialog Box Keyboard Interface</a>.


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-messages-and-message-queues">Creating a Message Loop</a>.

<div class="code"></div>

## -see-also

- <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-isdialogmessagea">IsDialogMessage</a>
- <a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-translateacceleratora">TranslateAccelerator</a>
- <a href="/windows/desktop/inputdev/wm-char">WM_CHAR</a>
- <a href="/windows/desktop/inputdev/wm-deadchar">WM_DEADCHAR</a>
- <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>
- <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>
- <a href="/windows/desktop/menurc/wm-syschar">WM_SYSCHAR</a>
- <a href="/windows/desktop/inputdev/wm-sysdeadchar">WM_SYSDEADCHAR</a>
- <a href="/windows/desktop/inputdev/wm-syskeydown">WM_SYSKEYDOWN</a>
- <a href="/windows/desktop/inputdev/wm-syskeyup">WM_SYSKEYUP</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>
