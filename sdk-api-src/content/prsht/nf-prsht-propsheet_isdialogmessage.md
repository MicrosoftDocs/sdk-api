---
UID: NF:prsht.PropSheet_IsDialogMessage
title: PropSheet_IsDialogMessage macro (prsht.h)
description: Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message. You can use this macro or send the PSM_ISDIALOGMESSAGE message explicitly.helpviewer_keywords: ["PropSheet_IsDialogMessage","PropSheet_IsDialogMessage macro [Windows Controls]","_win32_PropSheet_IsDialogMessage","_win32_PropSheet_IsDialogMessage_cpp","controls.PropSheet_IsDialogMessage","controls._win32_PropSheet_IsDialogMessage","prsht/PropSheet_IsDialogMessage"]
old-location: controls\PropSheet_IsDialogMessage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_isdialogmessage.htm
ms.date: 12/05/2018
ms.keywords: PropSheet_IsDialogMessage, PropSheet_IsDialogMessage macro [Windows Controls], _win32_PropSheet_IsDialogMessage, _win32_PropSheet_IsDialogMessage_cpp, controls.PropSheet_IsDialogMessage, controls._win32_PropSheet_IsDialogMessage, prsht/PropSheet_IsDialogMessage
f1_keywords:
- prsht/PropSheet_IsDialogMessage
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropSheet_IsDialogMessage macro


## -description


Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/psm-isdialogmessage">PSM_ISDIALOGMESSAGE</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.


### -param pMsg

Type: <b>LPMSG</b>

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that contains the message to be checked.


## -remarks



Your message loop should use the <b>PropSheet_IsDialogMessage</b> macro with modeless property sheets to pass messages to the property sheet dialog box. On systems that support Unicode, use the Unicode versions of the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> functions (<b>GetMessageW</b> and <b>PeekMessageW</b>) to retrieve messages.

If the return value indicates that the message was processed, it must not be passed to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-dispatchmessage">DispatchMessage</a> function.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a>
 

 

