---
UID: NF:prsht.PropSheet_IsDialogMessage
title: PropSheet_IsDialogMessage macro
author: windows-sdk-content
description: Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message. You can use this macro or send the PSM_ISDIALOGMESSAGE message explicitly.
old-location: controls\PropSheet_IsDialogMessage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_isdialogmessage.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: PropSheet_IsDialogMessage, PropSheet_IsDialogMessage macro [Windows Controls], _win32_PropSheet_IsDialogMessage, _win32_PropSheet_IsDialogMessage_cpp, controls.PropSheet_IsDialogMessage, controls._win32_PropSheet_IsDialogMessage, prsht/PropSheet_IsDialogMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: prsht.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PropSheet_IsDialogMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_IsDialogMessage macro


## -description


Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774593(v=VS.85).aspx">PSM_ISDIALOGMESSAGE</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


### -param pMsg

Type: <b>LPMSG</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a> structure that contains the message to be checked.


## -remarks



Your message loop should use the <b>PropSheet_IsDialogMessage</b> macro with modeless property sheets to pass messages to the property sheet dialog box. On systems that support Unicode, use the Unicode versions of the <a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a> and <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a> functions (<b>GetMessageW</b> and <b>PeekMessageW</b>) to retrieve messages.

If the return value indicates that the message was processed, it must not be passed to the <a href="https://msdn.microsoft.com/en-us/library/ms644955(v=VS.85).aspx">TranslateMessage</a> or <a href="https://msdn.microsoft.com/en-us/library/ms644934(v=VS.85).aspx">DispatchMessage</a> function.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/en-us/library/Bb774546(v=VS.85).aspx">PSH_AEROWIZARD</a>).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb760811(v=VS.85).aspx">PropertySheet</a>
 

 

