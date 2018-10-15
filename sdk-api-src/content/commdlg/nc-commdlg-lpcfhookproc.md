---
UID: NC:commdlg.LPCFHOOKPROC
title: LPCFHOOKPROC
author: windows-sdk-content
description: Receives messages or notifications intended for the default dialog box procedure of the Font dialog box. This is an application-defined or library-defined callback procedure that is used with the ChooseFont function.
old-location: dlgbox\cfhookproc.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\cfhookproc.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CFHookProc, LPCFHOOKPROC, LPCFHOOKPROC callback, LPCFHOOKPROC callback function [Dialog Boxes], _win32_CFHookProc, _win32_cfhookproc_cpp, commdlg/LPCFHOOKPROC, dlgbox.cfhookproc, winui._win32_cfhookproc
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
 - LPCFHOOKPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPCFHOOKPROC callback function


## -description


Receives messages or notifications intended for the default dialog box procedure of the <b>Font</b> dialog box. This is an application-defined or library-defined callback procedure that is used with the <a href="https://msdn.microsoft.com/a0565db0-8b18-4103-bf84-a21776043d7b">ChooseFont</a> function.

The <b>LPCFHOOKPROC</b> type defines a pointer to this callback function. <i>CFHookProc</i> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - hdlg [in]

A handle to the <b>Font</b> dialog box for which the message is intended.


#### - lParam [in]

Additional information about the message. The exact meaning depends on the value of the <i>uiMsg</i> parameter. If the <i>uiMsg</i> parameter indicates the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message, <i>lParam</i> is a pointer to a <a href="https://msdn.microsoft.com/a0565db0-8b18-4103-bf84-a21776043d7b">CHOOSEFONT</a> structure containing the values specified when the dialog box was created.


#### - uiMsg [in]

The identifier of the message being received.


#### - wParam [in]

Additional information about the message. The exact meaning depends on the value of the <i>uiMsg</i> parameter.


## -returns



If the hook procedure returns zero, the default dialog box procedure processes the message.

If the hook procedure returns a nonzero value, the default dialog box procedure ignores the message.




## -remarks



When you use the <a href="https://msdn.microsoft.com/a0565db0-8b18-4103-bf84-a21776043d7b">ChooseFont</a> function to create a <b>Font</b> dialog box, you can provide a <i>CFHookProc</i> hook procedure to process messages or notifications intended for the dialog box procedure. To enable the hook procedure, use the <b>CHOOSEFONT</b> structure that you passed to the dialog creation function. Specify the address of the hook procedure in the  <b>lpfnHook</b> member and specify the <b>CF_ENABLEHOOK</b> flag in the  <b>Flags</b> member.

The default dialog box procedure processes the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message before passing it to the hook procedure. For all other messages, the hook procedure receives the message first. The return value of the hook procedure determines whether the default dialog box procedure processes the message or ignores it.

If the hook procedure processes the <a href="https://msdn.microsoft.com/5b90ab3f-b751-486f-a0fa-33f791c31a26">WM_CTLCOLORDLG</a> message, it must return a valid brush handle to paint the background of the dialog box. In general, if the hook procedure processes any <b>WM_CTLCOLOR*</b> message, it must return a valid brush handle to paint the background of the specified control.

Do not call the <a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a> function from the hook procedure. Instead, the hook procedure can call the <a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a> function to post a <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> message with the <b>IDABORT</b> value to the dialog box procedure. Posting <b>IDABORT</b> closes the dialog box and causes the dialog box function to return <b>FALSE</b>. If you need to know why the hook procedure closed the dialog box, you must provide your own communication mechanism between the hook procedure and your application.

You can subclass the standard controls of a common dialog box. However, the dialog box procedure may also subclass the controls. Because of this, you should subclass controls when your hook procedure processes the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message. This ensures that your subclass procedure receives the control-specific messages before the subclass procedure set by the dialog box procedure.




## -see-also




<b>CHOOSEFONT</b>



<a href="https://msdn.microsoft.com/a0565db0-8b18-4103-bf84-a21776043d7b">ChooseFont</a>



<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a>



<a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/5b90ab3f-b751-486f-a0fa-33f791c31a26">WM_CTLCOLORDLG</a>



<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>
 

 

