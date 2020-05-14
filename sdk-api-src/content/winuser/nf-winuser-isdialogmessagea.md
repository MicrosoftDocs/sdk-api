---
UID: NF:winuser.IsDialogMessageA
title: IsDialogMessageA function (winuser.h)
description: Determines whether a message is intended for the specified dialog box and, if it is, processes the message.helpviewer_keywords: ["IsDialogMessage","IsDialogMessage function [Dialog Boxes]","IsDialogMessageA","IsDialogMessageW","_win32_IsDialogMessage","_win32_isdialogmessage_cpp","dlgbox.isdialogmessage","winui._win32_isdialogmessage","winuser/IsDialogMessage","winuser/IsDialogMessageA","winuser/IsDialogMessageW"]
old-location: dlgbox\isdialogmessage.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\isdialogmessage.htm
ms.date: 12/05/2018
ms.keywords: IsDialogMessage, IsDialogMessage function [Dialog Boxes], IsDialogMessageA, IsDialogMessageW, _win32_IsDialogMessage, _win32_isdialogmessage_cpp, dlgbox.isdialogmessage, winui._win32_isdialogmessage, winuser/IsDialogMessage, winuser/IsDialogMessageA, winuser/IsDialogMessageW
f1_keywords:
- winuser/IsDialogMessage
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IsDialogMessageW (Unicode) and IsDialogMessageA (ANSI)
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
- ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
- IsDialogMessage
- IsDialogMessageA
- IsDialogMessageW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsDialogMessageA function


## -description


Determines whether a message is intended for the specified dialog box and, if it is, processes the message. 


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box. 


### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that contains the message to be checked. 


## -returns



Type: <b>BOOL</b>

If the message has been processed, the return value is nonzero.

If the message has not been processed, the return value is zero. 




## -remarks



Although the <b>IsDialogMessage</b> function is intended for modeless dialog boxes, you can use it with any window that contains controls, enabling the windows to provide the same keyboard selection as is used in a dialog box. 

When <b>IsDialogMessage</b> processes a message, it checks for keyboard messages and converts them into selections for the corresponding dialog box. For example, the TAB key, when pressed, selects the next control or group of controls, and the DOWN ARROW key, when pressed, selects the next control in a group. 

Because the <b>IsDialogMessage</b> function performs all necessary translating and dispatching of messages, a message processed by <b>IsDialogMessage</b> must not be passed to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-dispatchmessage">DispatchMessage</a> function. 

<b>IsDialogMessage</b> sends <a href="https://docs.microsoft.com/windows/desktop/dlgbox/wm-getdlgcode">WM_GETDLGCODE</a> messages to the dialog box procedure to determine which keys should be processed. 

<b>IsDialogMessage</b> can send <a href="https://docs.microsoft.com/windows/desktop/dlgbox/dm-getdefid">DM_GETDEFID</a> and <a href="https://docs.microsoft.com/windows/desktop/dlgbox/dm-setdefid">DM_SETDEFID</a> messages to the window. These messages are defined in the Winuser.h header file as <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-user">WM_USER</a> and <b>WM_USER</b> + 1, so conflicts are possible with application-defined messages having the same values. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/dlgbox/dm-getdefid">DM_GETDEFID</a>



<a href="https://docs.microsoft.com/windows/desktop/dlgbox/dm-setdefid">DM_SETDEFID</a>



<a href="https://docs.microsoft.com/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-dispatchmessage">DispatchMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/dlgbox/wm-getdlgcode">WM_GETDLGCODE</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-user">WM_USER</a>
 

 

