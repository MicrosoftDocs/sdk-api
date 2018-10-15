---
UID: NF:commdlg.IPrintDialogCallback.HandleMessage
title: IPrintDialogCallback::HandleMessage
author: windows-sdk-content
description: Called by PrintDlgEx to give your application an opportunity to handle messages sent to the child dialog box in the lower portion of the General page of the Print Property Sheet.
old-location: dlgbox\iprintdialogcallback_handlemessage.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogcallback\iprintdialogcallbackhandlemessage.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: HandleMessage, HandleMessage method [Dialog Boxes], HandleMessage method [Dialog Boxes],IPrintDialogCallback interface, IPrintDialogCallback interface [Dialog Boxes],HandleMessage method, IPrintDialogCallback.HandleMessage, IPrintDialogCallback::HandleMessage, _win32_IPrintDialogCallback_HandleMessage, _win32_iprintdialogcallback_handlemessage_cpp, commdlg/IPrintDialogCallback::HandleMessage, dlgbox.iprintdialogcallback_handlemessage, winui._win32_iprintdialogcallback_handlemessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: commdlg.h
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
req.lib: 
req.dll: Comdlg32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comdlg32.dll
api_name:
 - IPrintDialogCallback.HandleMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrintDialogCallback::HandleMessage


## -description


Called by <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> to give your application an opportunity to handle messages sent to the child dialog box in the lower portion of the <b>General</b> page of the <a href="https://msdn.microsoft.com/b52b71cc-a583-4a21-8a53-501ab442e6f8">Print Property Sheet</a>. The child dialog box contains controls similar to those of the <b>Print</b> dialog box.


## -parameters




### -param hDlg

Type: <b>HWND</b>

A handle to the child dialog box in the lower portion of the <b>General</b> page.


### -param uMsg

Type: <b>UINT</b>

The identifier of the message being received.


### -param wParam

Type: <b>WPARAM</b>

Additional information about the message. The exact meaning depends on the value of the <i>uMsg</i> parameter.


### -param lParam

Type: <b>LPARAM</b>

Additional information about the message. The exact meaning depends on the value of the <i>uMsg</i> parameter.

					

If the <i>uMsg</i> parameter indicates the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message, <i>lParam</i> is a pointer to a <a href="https://msdn.microsoft.com/e843d2fc-d122-4112-bfc9-9bfb26e865da">PRINTDLGEX</a> structure containing the values specified when the property sheet was created.


### -param pResult

Type: <b>LRESULT*</b>

Indicates the result to be returned by the dialog box procedure for the message. The value pointed to should be <b>TRUE</b> if you process the message, otherwise it should be <b>FALSE</b> or whatever is an appropriate value according to the message type.


## -returns



Type: <b>HRESULT</b>

Return <b>S_OK</b> if your <b>IPrintDialogCallback::HandleMessage</b> implementation handled the message. In this case, the <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> function does not perform any default message handling.

Return <b>S_FALSE</b> if you want <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> to perform its default message handling.




## -remarks



For notification messages passed by the <a href="_win32_WM_NOTIFY">WM_NOTIFY</a> message, you must use the <a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a> function with the <b>DWL_MSGRESULT</b> value to set a return value. When you call <b>SetWindowLong</b>, use <a href="https://msdn.microsoft.com/9e1991dd-e451-4f2a-ac9f-069acb8e89c2">GetParent</a>(<i>hDlg</i>) to set the <b>DWL_MSGRESULT</b> value of the <b>General</b> page, which is the parent of the child window.

The default dialog box procedure for the child window in the lower portion of the <b>General</b> page processes the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message before passing it to the <b>HandleMessage</b> method. For all other messages sent to the child window, <b>HandleMessage</b> receives the message first. Then the <b>HandleMessage</b> return value determines whether the default dialog procedure processes the message or ignores it.

If <b>HandleMessage</b> processes the <a href="https://msdn.microsoft.com/5b90ab3f-b751-486f-a0fa-33f791c31a26">WM_CTLCOLORDLG</a> message, it must return a valid brush handle to painting the background of the dialog box. In general, if <b>HandleMessage</b> processes any <b>WM_CTLCOLOR*</b> message, it must return a valid brush handle to painting the background of the specified control.

Do not call the <a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a> function from the <b>HandleMessage</b> method. Instead, <b>HandleMessage</b> can call the <a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a> function to post a <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> message with the IDABORT value to the dialog box procedure. Posting <b>IDABORT</b> closes the <a href="https://msdn.microsoft.com/b52b71cc-a583-4a21-8a53-501ab442e6f8">Print Property Sheet</a> and causes <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> to return <b>PD_RESULT_CANCEL</b> in the <b>dwResultAction</b> member of the <a href="https://msdn.microsoft.com/e843d2fc-d122-4112-bfc9-9bfb26e865da">PRINTDLGEX</a> structure. If you need to know why <b>HandleMessage</b> closed the dialog box, you must provide your own communication mechanism between the <b>HandleMessage</b> method and your application.

You can subclass the standard controls of the child dialog box in the lower portion of the <b>General</b> page. These standard controls are similar to those found in the <b>Print</b> dialog box. However, the default dialog box procedure may also subclass the controls. Because of this, you should subclass controls when <b>HandleMessage</b> processes the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message. This ensures that your subclass procedure receives control-specific messages before the subclass procedure set by the dialog box procedure.




## -see-also




<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a>



<a href="https://msdn.microsoft.com/51902f34-d0ab-4b49-9302-a8e6e9bd7061">IPrintDialogCallback</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/e843d2fc-d122-4112-bfc9-9bfb26e865da">PRINTDLGEX</a>



<a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a>



<a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a>



<a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a>



<a href="https://msdn.microsoft.com/5b90ab3f-b751-486f-a0fa-33f791c31a26">WM_CTLCOLORDLG</a>



<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>



<a href="_win32_WM_NOTIFY">WM_NOTIFY</a>
 

 

