---
UID: NC:commdlg.LPPAGESETUPHOOK
title: LPPAGESETUPHOOK (commdlg.h)
description: Receives messages or notifications intended for the default dialog box procedure of the Page Setup dialog box. The PageSetupHook hook procedure is an application-defined or library-defined callback function used with the PageSetupDlg function.
helpviewer_keywords: ["LPPAGESETUPHOOK","LPPAGESETUPHOOK callback","LPPAGESETUPHOOK callback function [Dialog Boxes]","_win32_PageSetupHook","_win32_pagesetuphook_cpp","commdlg/LPPAGESETUPHOOK","dlgbox.pagesetuphook","winui._win32_pagesetuphook"]
old-location: dlgbox\pagesetuphook.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\pagesetuphook.htm
ms.date: 12/05/2018
ms.keywords: LPPAGESETUPHOOK, LPPAGESETUPHOOK callback, LPPAGESETUPHOOK callback function [Dialog Boxes], _win32_PageSetupHook, _win32_pagesetuphook_cpp, commdlg/LPPAGESETUPHOOK, dlgbox.pagesetuphook, winui._win32_pagesetuphook
f1_keywords:
- commdlg/LPPAGESETUPHOOK
dev_langs:
- c++
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
- LPPAGESETUPHOOK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPPAGESETUPHOOK callback function


## -description


Receives messages or notifications intended for the default dialog box procedure of the <b>Page Setup</b> dialog box. The <i>PageSetupHook</i> hook procedure is an application-defined or library-defined callback function used with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a> function.

The <b>LPPAGESETUPHOOK</b> type defines a pointer to this callback function. <i>PageSetupHook</i> is a placeholder for the application-defined or library-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - hdlg [in]

A handle to the <b>Page Setup</b> dialog box for which the message is intended.


#### - lParam [in]

Additional information about the message. The exact meaning depends on the value of the <i>uiMsg</i> parameter. 

If the <i>uiMsg</i> parameter indicates the <a href="https://docs.microsoft.com/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message, <i>lParam</i> is a pointer to a <a href="/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga">PAGESETUPDLG</a> structure containing the values specified when the dialog box was created.


#### - uiMsg [in]

The identifier of the message being received.


#### - wParam [in]

Additional information about the message. The exact meaning depends on the value of the <i>uiMsg</i> parameter.


## -returns



If the hook procedure returns zero, the default dialog box procedure processes the message.

If the hook procedure returns a nonzero value, the default dialog box procedure ignores the message.




## -remarks



When you use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a> function to create a <b>Page Setup</b> dialog box, you can provide a <i>PageSetupHook</i> hook procedure to process messages or notifications intended for the dialog box procedure. To enable the hook procedure, use the <a href="/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga">PAGESETUPDLG</a> structure that you passed to the dialog creation function. Specify the pointer to the hook procedure in the  <b>lpfnPageSetupHook</b> member and specify the <b>PSD_ENABLEPAGESETUPHOOK</b> flag in the  <b>Flags</b> member.

The default dialog box procedure processes the <a href="https://docs.microsoft.com/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message before passing it to the hook procedure. For all other messages, the hook procedure receives the message first. Then, the return value of the hook procedure determines whether the default dialog procedure processes the message or ignores it.

If the hook procedure processes the <a href="https://docs.microsoft.com/windows/desktop/dlgbox/wm-ctlcolordlg">WM_CTLCOLORDLG</a> message, it must return a valid brush handle to painting the background of the dialog box. In general, if the hook procedure processes any <b>WM_CTLCOLOR*</b> message, it must return a valid brush handle to painting the background of the specified control.

Do not call the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a> function from the hook procedure. Instead, the hook procedure can call the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> function to post a  <a href="https://docs.microsoft.com/windows/desktop/menurc/wm-command">WM_COMMAND</a> message with the <b>IDABORT</b> value to the dialog box procedure. Posting <b>IDABORT</b> closes the dialog box and causes the dialog box function to return <b>FALSE</b>. If you need to know why the hook procedure closed the dialog box, you must provide your own communication mechanism between the hook procedure and your application.

You can subclass the standard controls of a common dialog box. However, the dialog box procedure may also subclass the controls. Because of this, you should subclass controls when your hook procedure processes the <a href="https://docs.microsoft.com/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message. This ensures that your subclass procedure receives the control-specific messages before the subclass procedure set by the dialog box procedure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a>



<a href="/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga">PAGESETUPDLG</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/dlgbox/wm-ctlcolordlg">WM_CTLCOLORDLG</a>



<a href="https://docs.microsoft.com/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>
 

 

