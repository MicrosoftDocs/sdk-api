---
UID: NC:commdlg.LPSETUPHOOKPROC
title: LPSETUPHOOKPROC (commdlg.h)
author: windows-sdk-content
description: An application-defined or library-defined callback function used with the PrintDlg function. The hook procedure receives messages or notifications intended for the default dialog box procedure of the Print Setup dialog box.
old-location: dlgbox\setuphookproc.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\setuphookproc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LPSETUPHOOKPROC, LPSETUPHOOKPROC callback, LPSETUPHOOKPROC callback function [Dialog Boxes], _win32_SetupHookProc, _win32_setuphookproc_cpp, commdlg/LPSETUPHOOKPROC, dlgbox.setuphookproc, winui._win32_setuphookproc
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
 - LPSETUPHOOKPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPSETUPHOOKPROC callback function


## -description


An application-defined or library-defined callback function used with the <a href="https://msdn.microsoft.com/en-us/library/ms646940(v=VS.85).aspx">PrintDlg</a> function. The hook procedure receives messages or notifications intended for the default dialog box procedure of the <b>Print Setup</b> dialog box.

The <b>LPSETUPHOOKPROC</b> type defines a pointer to this callback function. <i>SetupHookProc</i> is a placeholder for the application-defined or library-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - hdlg [in]

A handle to the <b>Print Setup</b> dialog box for which the message is intended.


#### - lParam [in]

Additional information about the message. The exact meaning depends on the value of the <i>uiMsg</i> parameter.


#### - uiMsg [in]

The identifier of the message being received.


#### - wParam [in]

Additional information about the message. The exact meaning depends on the value of the <i>uiMsg</i> parameter.


## -returns



If the hook procedure returns zero, the default dialog box procedure processes the message.

If the hook procedure returns a nonzero value, the default dialog box procedure ignores the message.




## -remarks



The <b>Print Setup</b> dialog box has been superseded by the <b>Page Setup</b> dialog box, which should be used by new applications. However, for compatibility, the <a href="https://msdn.microsoft.com/en-us/library/ms646940(v=VS.85).aspx">PrintDlg</a> function continues to support display of the <b>Print Setup</b> dialog box. You can provide a <i>SetupHookProc</i> hook procedure for the <b>Print Setup</b> dialog box to process messages or notifications intended for the dialog box procedure.

To enable the hook procedure, use the <a href="https://msdn.microsoft.com/en-us/library/ms646843(v=VS.85).aspx">PRINTDLG</a> structure that you passed to the dialog creation function. Specify the address of the hook procedure in the  <b>lpfnSetupHook</b> member and specify the <b>PD_ENABLESETUPHOOK</b> flag in the  <b>Flags</b> member.

The default dialog box procedure processes the <a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a> message before passing it to the hook procedure. For all other messages, the hook procedure receives the message first. Then, the return value of the hook procedure determines whether the default dialog procedure processes the message or ignores it.

If the hook procedure processes the <a href="https://msdn.microsoft.com/en-us/library/ms645417(v=VS.85).aspx">WM_CTLCOLORDLG</a> message, it must return a valid brush handle to painting the background of the dialog box. In general, if the hook procedure processes any <b>WM_CTLCOLOR*</b> message, it must return a valid brush handle to painting the background of the specified control.

Do not call the <a href="https://msdn.microsoft.com/en-us/library/ms645472(v=VS.85).aspx">EndDialog</a> function from the hook procedure. Instead, the hook procedure can call the <a href="https://msdn.microsoft.com/en-us/library/ms644944(v=VS.85).aspx">PostMessage</a> function to post a  <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> message with the <b>IDABORT</b> value to the dialog box procedure. Posting <b>IDABORT</b> closes the dialog box and causes the dialog box function to return <b>FALSE</b>. If you need to know why the hook procedure closed the dialog box, you must provide your own communication mechanism between the hook procedure and your application.

You can subclass the standard controls of a common dialog box. However, the dialog box procedure may also subclass the controls. Because of this, you should subclass controls when your hook procedure processes the <a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a> message. This ensures that your subclass procedure receives the control-specific messages before the subclass procedure set by the dialog box procedure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms645524(v=VS.85).aspx">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645472(v=VS.85).aspx">EndDialog</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646843(v=VS.85).aspx">PRINTDLG</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644944(v=VS.85).aspx">PostMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646940(v=VS.85).aspx">PrintDlg</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645417(v=VS.85).aspx">WM_CTLCOLORDLG</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a>
 

 

