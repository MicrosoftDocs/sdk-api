---
UID: NF:winuser.RegisterWindowMessageW
title: RegisterWindowMessageW function (winuser.h)
author: windows-sdk-content
description: Defines a new window message that is guaranteed to be unique throughout the system. The message value can be used when sending or posting messages.
old-location: winmsg\registerwindowmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\registerwindowmessage.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RegisterWindowMessage, RegisterWindowMessage function [Windows and Messages], RegisterWindowMessageA, RegisterWindowMessageW, _win32_RegisterWindowMessage, _win32_registerwindowmessage_cpp, winmsg.registerwindowmessage, winui._win32_registerwindowmessage, winuser/RegisterWindowMessage, winuser/RegisterWindowMessageA, winuser/RegisterWindowMessageW
ms.topic: function
f1_keywords: 
 - "winuser/RegisterWindowMessage"
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegisterWindowMessageW (Unicode) and RegisterWindowMessageA (ANSI)
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
 - RegisterWindowMessage
 - RegisterWindowMessageA
 - RegisterWindowMessageW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegisterWindowMessageW function


## -description


Defines a new window message that is guaranteed to be unique throughout the system. The message value can be used when sending or posting messages.


## -parameters




### -param lpString [in]

Type: <b>LPCTSTR</b>

The message to be registered.


## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

If the message is successfully registered, the return value is a message identifier in the range 0xC000 through 0xFFFF.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <b>RegisterWindowMessage</b> function is typically used to register messages for communicating between two cooperating applications. 

If two different applications register the same message string, the applications return the same message value. The message remains registered until the session ends. 

Only use <b>RegisterWindowMessage</b> when more than one application must process the same message. For sending private messages within a window class, an application can use any integer in the range <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-user">WM_USER</a> through 0x7FFF. (Messages in this range are private to a window class, not to an application. For example, predefined control classes such as <b>BUTTON</b>, <b>EDIT</b>, <b>LISTBOX</b>, and <b>COMBOBOX</b> may use values in this range.) 


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/dlgbox/using-common-dialog-boxes">Finding Text</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>
 

 

