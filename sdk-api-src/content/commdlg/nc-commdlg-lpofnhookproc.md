---
UID: NC:commdlg.LPOFNHOOKPROC
title: LPOFNHOOKPROC
author: windows-sdk-content
description: Receives notification messages sent from the dialog box.
old-location: dlgbox\ofnhookproc.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\ofnhookproc.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: LPOFNHOOKPROC, LPOFNHOOKPROC callback, LPOFNHOOKPROC callback function [Dialog Boxes], _win32_OFNHookProc, _win32_ofnhookproc_cpp, commdlg/LPOFNHOOKPROC, dlgbox.ofnhookproc, winui._win32_ofnhookproc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Commdlg.h
api_name:
 - LPOFNHOOKPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPOFNHOOKPROC callback function


## -description


<p class="CCE_Message">[Starting with Windows Vista, the <b>Open</b> and <b>Save As</b> common dialog boxes have been superseded by the <a href="_shell_common_file_dialog">Common Item Dialog</a>. We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.]

Receives notification messages sent from the dialog box. The function also receives messages for any additional controls that you defined by specifying a child dialog template. The <i>OFNHookProc</i> hook procedure is an application-defined or library-defined callback function that is used with the Explorer-style <b>Open</b> and <b>Save As</b> dialog boxes.

The <b>LPOFNHOOKPROC</b> type defines a pointer to this callback function. <i>OFNHookProc</i> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - hdlg [in]

A handle to the child dialog box of the <b>Open</b> or <b>Save As</b> dialog box. Use the <a href="https://msdn.microsoft.com/9e1991dd-e451-4f2a-ac9f-069acb8e89c2">GetParent</a> function to get the handle to the <b>Open</b> or <b>Save As</b> dialog box.


#### - lParam [in]

Additional information about the message. The exact meaning depends on the value of the <i>uiMsg</i> parameter. If the <i>uiMsg</i> parameter indicates the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message, <i>lParam</i> is a pointer to an <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure containing the values specified when the dialog box was created.


#### - uiMsg [in]

The identifier of the message being received.


#### - wParam [in]

Additional information about the message. The exact meaning depends on the value of the <i>uiMsg</i> parameter.


## -returns



If the hook procedure returns zero, the default dialog box procedure processes the message.

                    

If the hook procedure returns a nonzero value, the default dialog box procedure ignores the message.

For the <a href="https://msdn.microsoft.com/a62ca550-0997-4379-aaaf-a5bc9414bd69">CDN_SHAREVIOLATION</a> and <a href="https://msdn.microsoft.com/7f3de96f-68d8-4f40-b74f-304835f9def2">CDN_FILEOK</a> notification messages, the hook procedure should return a nonzero value to indicate that it has used the <a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a> function to set a nonzero <b>DWL_MSGRESULT</b> value.




## -remarks



If you do not specify the <b>OFN_EXPLORER</b> flag when you create an <b>Open</b> or <b>Save As</b> dialog box, and you want a hook procedure, you must use an old-style <a href="https://msdn.microsoft.com/ee551824-51f9-422d-9741-96248e3fc8cc">OFNHookProcOldStyle</a> hook procedure. In this case, the dialog box will have the old-style user interface.

When you use the <a href="https://msdn.microsoft.com/22b8f3d0-455a-4eb8-9835-e90d41924ec7">GetOpenFileName</a> or <a href="https://msdn.microsoft.com/424e9d85-853b-4dc6-a29a-c532a8bb23f7">GetSaveFileName</a> functions to create an Explorer-style <b>Open</b> or <b>Save As</b> dialog box, you can provide an <i>OFNHookProc</i> hook procedure. To enable the hook procedure, use the <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure that you passed to the dialog creation function. Specify the pointer to the hook procedure in the  <b>lpfnHook</b> member and specify the <b>OFN_ENABLEHOOK</b> flag in the  <b>Flags</b> member.

If you provide a hook procedure for an Explorer-style common dialog box, the system creates a dialog box that is a child of the default dialog box. The hook procedure acts as the dialog procedure for the child dialog. This child dialog is based on the template you specified in the <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure, or it is a default child dialog if no template is specified. The child dialog is created when the default dialog procedure is processing its <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message. After the child dialog processes its own <b>WM_INITDIALOG</b> message, the default dialog procedure moves the standard controls, if necessary, to make room for any additional controls of the child dialog. The system then sends the <a href="https://msdn.microsoft.com/337fccac-5444-442d-92f0-862c5302fa21">CDN_INITDONE</a> notification message to the hook procedure.

The hook procedure does not receive messages intended for the standard controls of the default dialog box. You can subclass the standard controls, but this is discouraged because it may make your application incompatible with later versions. However, the Explorer-style common dialog boxes provide a set of messages that the hook procedure can use to monitor and control the dialog. These include a set of notification messages sent from the dialog, as well as messages that you can send to retrieve information from the dialog. For a complete list of these messages, see <a href="open_and_save_as_dialog_boxes.htm">Explorer-Style Hook Procedures</a>.

If the hook procedure processes the <a href="https://msdn.microsoft.com/5b90ab3f-b751-486f-a0fa-33f791c31a26">WM_CTLCOLORDLG</a> message, it must return a valid brush handle to painting the background of the dialog box. In general, if it processes any <b>WM_CTLCOLOR*</b> message, it must return a valid brush handle to painting the background of the specified control.

Do not call the <a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a> function from the hook procedure. Instead, the hook procedure can call the <a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a> function to post a  <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> message with the <b>IDCANCEL</b> value to the dialog box procedure. Posting <b>IDCANCEL</b> closes the dialog box and causes the dialog box function to return <b>FALSE</b>. If you need to know why the hook procedure closed the dialog box, you must provide your own communication mechanism between the hook procedure and your application.




## -see-also




<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/22b8f3d0-455a-4eb8-9835-e90d41924ec7">GetOpenFileName</a>



<a href="https://msdn.microsoft.com/424e9d85-853b-4dc6-a29a-c532a8bb23f7">GetSaveFileName</a>



<a href="https://msdn.microsoft.com/ee551824-51f9-422d-9741-96248e3fc8cc">OFNHookProcOldStyle</a>



<a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a>



<b>Reference</b>
 

 

