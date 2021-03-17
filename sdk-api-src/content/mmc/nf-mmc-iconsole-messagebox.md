---
UID: NF:mmc.IConsole.MessageBox
title: IConsole::MessageBox (mmc.h)
description: Displays a message box.
helpviewer_keywords: ["IConsole interface [MMC]","MessageBox method","IConsole.MessageBox","IConsole::MessageBox","MB_ABORTRETRYIGNORE","MB_APPLMODAL","MB_DEFAULT_DESKTOP_ONLY","MB_DEFBUTTON1","MB_DEFBUTTON2","MB_DEFBUTTON3","MB_DEFBUTTON4","MB_HELP","MB_ICONEXCLAMATION","MB_ICONWARNING","MB_ICONINFORMATION","MB_ICONASTERISK","MB_ICONQUESTION","MB_ICONSTOP","MB_ICONERROR","MB_ICONHAND","MB_OK","MB_OKCANCEL","MB_RETRYCANCEL","MB_RIGHT","MB_RTLREADING","MB_SERVICE_NOTIFICATION","MB_SERVICE_NOTIFICATION_NT3x","MB_SETFOREGROUND","MB_SYSTEMMODAL","MB_TASKMODAL","MB_TOPMOST","MB_YESNO","MB_YESNOCANCEL","MessageBox","MessageBox method [MMC]","MessageBox method [MMC]","IConsole interface","mmc.iconsole_messagebox","mmc/IConsole::MessageBox"]
old-location: mmc\iconsole_messagebox.htm
tech.root: mmc
ms.assetid: 37F5BF57-A2F6-41BB-822D-298BBCF28B45
ms.date: 12/05/2018
ms.keywords: IConsole interface [MMC],MessageBox method, IConsole.MessageBox, IConsole::MessageBox, MB_ABORTRETRYIGNORE, MB_APPLMODAL, MB_DEFAULT_DESKTOP_ONLY, MB_DEFBUTTON1, MB_DEFBUTTON2, MB_DEFBUTTON3, MB_DEFBUTTON4, MB_HELP, MB_ICONEXCLAMATION,MB_ICONWARNING, MB_ICONINFORMATION,MB_ICONASTERISK, MB_ICONQUESTION, MB_ICONSTOP,MB_ICONERROR,MB_ICONHAND, MB_OK, MB_OKCANCEL, MB_RETRYCANCEL, MB_RIGHT, MB_RTLREADING, MB_SERVICE_NOTIFICATION, MB_SERVICE_NOTIFICATION_NT3x, MB_SETFOREGROUND, MB_SYSTEMMODAL, MB_TASKMODAL, MB_TOPMOST, MB_YESNO, MB_YESNOCANCEL, MessageBox, MessageBox method [MMC], MessageBox method [MMC],IConsole interface, mmc.iconsole_messagebox, mmc/IConsole::MessageBox
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConsole::MessageBox
 - mmc/IConsole::MessageBox
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsole.MessageBox
---

# IConsole::MessageBox


## -description

Displays a message box.

## -parameters

### -param lpszText [in]

A pointer to a null-terminated string that contains the message to be displayed.

### -param lpszTitle [in]

A pointer to a null-terminated string used for the message box title. If this parameter is <b>NULL</b>, the default title "Error" is used.

### -param fuStyle [in]

A value that specifies a set of bit flags that determine the contents and behavior of the message box. This parameter can be a combination of flags from the following groups of flags taken from the documentation for the Windows API 
<a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a>.

Specify one of the following flags to indicate which buttons appear in the message box.



#### MB_ABORTRETRYIGNORE

The message box contains three buttons: Abort, Retry, and Ignore.



#### MB_OK

The message box contains one button: OK. This is the default.



#### MB_OKCANCEL

The message box contains two buttons: OK and 
Cancel.



#### MB_RETRYCANCEL

The message box contains two buttons: Retry and 
Cancel.



#### MB_YESNO

The message box contains two buttons: Yes and No.



#### MB_YESNOCANCEL

The message box contains three buttons: Yes, No, and 
Cancel.

Specify one of the following flags to indicate which icon appears in the message box:



#### MB_ICONEXCLAMATION, MB_ICONWARNING

An exclamation point icon appears in the message box.



#### MB_ICONINFORMATION, MB_ICONASTERISK

An icon consisting of an "I" in a circle appears in the message box.



#### MB_ICONQUESTION

A question-mark icon appears in the message box.



#### MB_ICONSTOP,
MB_ICONERROR,
MB_ICONHAND

A stop sign icon appears in the message box.

Specify one of the following flags to indicate the default button:



#### MB_DEFBUTTON1

The first button is the default button unless one of the other flags in this group is specified as the default.



#### MB_DEFBUTTON2

The second button is the default button.



#### MB_DEFBUTTON3

The third button is the default button.



#### MB_DEFBUTTON4

The fourth button is the default button.

Specify one of the following flags to indicate the modality of the dialog box:



#### MB_APPLMODAL

The user must respond to the message box before continuing work in the current window. However, the user can move to the windows of other applications and work in those windows. The default is <b>MB_APPLMODAL</b> if neither <b>MB_SYSTEMMODAL</b> nor <b>MB_TASKMODAL</b> is specified.



#### MB_SYSTEMMODAL

All applications are suspended until the user responds to the message box. System-modal message boxes are used to notify the user of serious, potentially damaging errors that require immediate attention and should be used sparingly.



#### MB_TASKMODAL

Similar to <b>MB_APPLMODAL</b>, but not useful within a Microsoft Foundation Classes (MFC) application. This flag is reserved for a calling application or library that does not have a window handle available.

In addition, you can specify the following flags:



#### MB_DEFAULT_DESKTOP_ONLY

The desktop currently receiving input must be a default desktop; otherwise, the function fails. A default desktop is one an application runs on after the user has logged on.



#### MB_HELP

Adds a 
<b>Help</b> button to the message box. Choosing the 
<b>Help</b> button or pressing <b>F1</b> generates a Help event.



#### MB_RIGHT

The text is right-justified.



#### MB_RTLREADING

Displays message and caption text using right-to-left reading order for Hebrew and Arabic systems.



#### MB_SETFOREGROUND

The message box becomes the foreground window. Internally, the operating system calls the <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a> function for the message box.



#### MB_TOPMOST

The message box is created with the <b>WS_EX_TOPMOST</b> window style.



#### MB_SERVICE_NOTIFICATION

The caller is a service notifying the user of an event. The function displays a message box on the current active desktop, even if there is no user logged on to the computer.

For more information about using this flag, see the <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a> function.



#### MB_SERVICE_NOTIFICATION_NT3x

This value corresponds to the value defined for <b>MB_SERVICE_NOTIFICATION</b> for earlier versions of Windows.

### -param piRetval [out]

A pointer to the return value.

## -returns

This method can return one of these values.

## -remarks

<b>MessageBox</b> should not be used for that displays errors that occur when the snap-in does not have the focus. Generally, 

<b>MessageBox</b> should be used only when the error demands user attention and when the result pane contains useful information despite the error.

In most cases, the MMC message OCX control is a more appropriate way of that displays error messages. For more information, see 
<a href="/previous-versions/windows/desktop/mmc/using-the-mmc-message-ocx-control">Using the MMC Message OCX Control</a>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a>