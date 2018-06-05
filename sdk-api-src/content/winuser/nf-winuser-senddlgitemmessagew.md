---
UID: NF:winuser.SendDlgItemMessageW
title: SendDlgItemMessageW function
author: windows-sdk-content
description: Sends a message to the specified control in a dialog box.
old-location: dlgbox\senddlgitemmessage.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\senddlgitemmessage.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: SendDlgItemMessage, SendDlgItemMessage function [Dialog Boxes], SendDlgItemMessageA, SendDlgItemMessageW, _win32_SendDlgItemMessage, _win32_senddlgitemmessage_cpp, dlgbox.senddlgitemmessage, winui._win32_senddlgitemmessage, winuser/SendDlgItemMessage, winuser/SendDlgItemMessageA, winuser/SendDlgItemMessageW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	Ext-MS-Win-NTUser-DialogBox-l1-1-0.dll
-	Ext-MS-Win-NTUser-DialogBox-l1-1-1.dll
-	ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
-	SendDlgItemMessage
-	SendDlgItemMessageA
-	SendDlgItemMessageW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SendDlgItemMessageW function


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

For lists of the system-provided messages, see <a href="https://msdn.microsoft.com/21a4d40b-52da-49e4-a374-afc4927e96e8">System-Defined Messages</a>.


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

Using <b>SendDlgItemMessage</b> is identical to retrieving a handle to the specified control and calling the <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a> function. 


#### Examples


			
			For an example, see <a href="using_dialog_boxes.htm">Creating a Modeless Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a>
 

 

