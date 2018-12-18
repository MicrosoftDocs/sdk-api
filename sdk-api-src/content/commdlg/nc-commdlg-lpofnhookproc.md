---
UID: NC:commdlg.LPOFNHOOKPROC
title: LPOFNHOOKPROC
author: windows-sdk-content
description: Receives notification messages sent from the dialog box.
old-location: dlgbox\ofnhookproc.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\ofnhookproc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LPOFNHOOKPROC, LPOFNHOOKPROC callback, LPOFNHOOKPROC callback function [Dialog Boxes], _win32_OFNHookProc, _win32_ofnhookproc_cpp, commdlg/LPOFNHOOKPROC, dlgbox.ofnhookproc, winui._win32_ofnhookproc
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


<p class="CCE_Message">[Starting with Windows Vista, the <b>Open</b> and <b>Save As</b> common dialog boxes have been superseded by the <a href="https://msdn.microsoft.com/en-us/library/Bb776913(v=VS.85).aspx">Common Item Dialog</a>. We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.]

Receives notification messages sent from the dialog box. The function also receives messages for any additional controls that you defined by specifying a child dialog template. The <i>OFNHookProc</i> hook procedure is an application-defined or library-defined callback function that is used with the Explorer-style <b>Open</b> and <b>Save As</b> dialog boxes.

The <b>LPOFNHOOKPROC</b> type defines a pointer to this callback function. <i>OFNHookProc</i> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - hdlg [in]

A handle to the child dialog box of the <b>Open</b> or <b>Save As</b> dialog box. Use the <a href="https://msdn.microsoft.com/en-us/library/ms633510(v=VS.85).aspx">GetParent</a> function to get the handle to the <b>Open</b> or <b>Save As</b> dialog box.


#### - lParam [in]

Additional information about the message. The exact meaning depends on the value of the <i>uiMsg</i> parameter. If the <i>uiMsg</i> parameter indicates the <a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a> message, <i>lParam</i> is a pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a> structure containing the values specified when the dialog box was created.


#### - uiMsg [in]

The identifier of the message being received.


#### - wParam [in]

Additional information about the message. The exact meaning depends on the value of the <i>uiMsg</i> parameter.


## -returns



If the hook procedure returns zero, the default dialog box procedure processes the message.

                    

If the hook procedure returns a nonzero value, the default dialog box procedure ignores the message.

For the <a href="https://msdn.microsoft.com/en-us/library/ms646866(v=VS.85).aspx">CDN_SHAREVIOLATION</a> and <a href="https://msdn.microsoft.com/en-us/library/ms646857(v=VS.85).aspx">CDN_FILEOK</a> notification messages, the hook procedure should return a nonzero value to indicate that it has used the <a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a> function to set a nonzero <b>DWL_MSGRESULT</b> value.




## -remarks



If you do not specify the <b>OFN_EXPLORER</b> flag when you create an <b>Open</b> or <b>Save As</b> dialog box, and you want a hook procedure, you must use an old-style <a href="https://msdn.microsoft.com/ee551824-51f9-422d-9741-96248e3fc8cc">OFNHookProcOldStyle</a> hook procedure. In this case, the dialog box will have the old-style user interface.

When you use the <a href="https://msdn.microsoft.com/en-us/library/ms646927(v=VS.85).aspx">GetOpenFileName</a> or <a href="https://msdn.microsoft.com/en-us/library/ms646928(v=VS.85).aspx">GetSaveFileName</a> functions to create an Explorer-style <b>Open</b> or <b>Save As</b> dialog box, you can provide an <i>OFNHookProc</i> hook procedure. To enable the hook procedure, use the <a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a> structure that you passed to the dialog creation function. Specify the pointer to the hook procedure in the  <b>lpfnHook</b> member and specify the <b>OFN_ENABLEHOOK</b> flag in the  <b>Flags</b> member.

If you provide a hook procedure for an Explorer-style common dialog box, the system creates a dialog box that is a child of the default dialog box. The hook procedure acts as the dialog procedure for the child dialog. This child dialog is based on the template you specified in the <a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a> structure, or it is a default child dialog if no template is specified. The child dialog is created when the default dialog procedure is processing its <a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a> message. After the child dialog processes its own <b>WM_INITDIALOG</b> message, the default dialog procedure moves the standard controls, if necessary, to make room for any additional controls of the child dialog. The system then sends the <a href="https://msdn.microsoft.com/en-us/library/ms646863(v=VS.85).aspx">CDN_INITDONE</a> notification message to the hook procedure.

The hook procedure does not receive messages intended for the standard controls of the default dialog box. You can subclass the standard controls, but this is discouraged because it may make your application incompatible with later versions. However, the Explorer-style common dialog boxes provide a set of messages that the hook procedure can use to monitor and control the dialog. These include a set of notification messages sent from the dialog, as well as messages that you can send to retrieve information from the dialog. For a complete list of these messages, see <a href="https://msdn.microsoft.com/en-us/library/ms646960(v=VS.85).aspx">Explorer-Style Hook Procedures</a>.

If the hook procedure processes the <a href="https://msdn.microsoft.com/en-us/library/ms645417(v=VS.85).aspx">WM_CTLCOLORDLG</a> message, it must return a valid brush handle to painting the background of the dialog box. In general, if it processes any <b>WM_CTLCOLOR*</b> message, it must return a valid brush handle to painting the background of the specified control.

Do not call the <a href="https://msdn.microsoft.com/en-us/library/ms645472(v=VS.85).aspx">EndDialog</a> function from the hook procedure. Instead, the hook procedure can call the <a href="https://msdn.microsoft.com/en-us/library/ms644944(v=VS.85).aspx">PostMessage</a> function to post a  <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> message with the <b>IDCANCEL</b> value to the dialog box procedure. Posting <b>IDCANCEL</b> closes the dialog box and causes the dialog box function to return <b>FALSE</b>. If you need to know why the hook procedure closed the dialog box, you must provide your own communication mechanism between the hook procedure and your application.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms645524(v=VS.85).aspx">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646927(v=VS.85).aspx">GetOpenFileName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646928(v=VS.85).aspx">GetSaveFileName</a>



<a href="https://msdn.microsoft.com/ee551824-51f9-422d-9741-96248e3fc8cc">OFNHookProcOldStyle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a>



<b>Reference</b>
 

 

