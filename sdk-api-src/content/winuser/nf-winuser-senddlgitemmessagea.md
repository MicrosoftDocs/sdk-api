---
UID: NF:winuser.SendDlgItemMessageA
title: SendDlgItemMessageA function (winuser.h)
description: Sends a message to the specified control in a dialog box.helpviewer_keywords: ["SendDlgItemMessage","SendDlgItemMessage function [Dialog Boxes]","SendDlgItemMessageA","SendDlgItemMessageW","_win32_SendDlgItemMessage","_win32_senddlgitemmessage_cpp","dlgbox.senddlgitemmessage","winui._win32_senddlgitemmessage","winuser/SendDlgItemMessage","winuser/SendDlgItemMessageA","winuser/SendDlgItemMessageW"]
old-location: dlgbox\senddlgitemmessage.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\senddlgitemmessage.htm
ms.date: 12/05/2018
ms.keywords: SendDlgItemMessage, SendDlgItemMessage function [Dialog Boxes], SendDlgItemMessageA, SendDlgItemMessageW, _win32_SendDlgItemMessage, _win32_senddlgitemmessage_cpp, dlgbox.senddlgitemmessage, winui._win32_senddlgitemmessage, winuser/SendDlgItemMessage, winuser/SendDlgItemMessageA, winuser/SendDlgItemMessageW
f1_keywords:
- winuser/SendDlgItemMessage
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
req.unicode-ansi: SendDlgItemMessageW (Unicode) and SendDlgItemMessageA (ANSI)
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
- Ext-MS-Win-NTUser-DialogBox-l1-1-0.dll
- Ext-MS-Win-NTUser-DialogBox-l1-1-1.dll
- ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
- SendDlgItemMessage
- SendDlgItemMessageA
- SendDlgItemMessageW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SendDlgItemMessageA function


## -description


Sends a message to the specified control in a dialog box.


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box that contains the control. 


### -param nIDDlgItem [in]

Type: <b>int</b>

The identifier of the control that receives the message. 


### -param Msg [in]

Type: <b>UINT</b>

The message to be sent.

For lists of the system-provided messages, see <a href="https://docs.microsoft.com/windows/desktop/winmsg/about-messages-and-message-queues">System-Defined Messages</a>.


### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information. 


### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information. 


## -returns



Type: <b>LRESULT</b>

The return value specifies the result of the message processing and depends on the message sent. 




## -remarks



The <b>SendDlgItemMessage</b> function does not return until the message has been processed. 

Using <b>SendDlgItemMessage</b> is identical to retrieving a handle to the specified control and calling the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function. 


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/dlgbox/using-dialog-boxes">Creating a Modeless Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>
 

 

