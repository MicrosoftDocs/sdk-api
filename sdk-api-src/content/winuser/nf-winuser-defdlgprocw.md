---
UID: NF:winuser.DefDlgProcW
title: DefDlgProcW function
author: windows-sdk-content
description: Calls the default dialog box window procedure to provide default processing for any window messages that a dialog box with a private window class does not process.
old-location: dlgbox\defdlgproc.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\defdlgproc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DefDlgProc, DefDlgProc function [Dialog Boxes], DefDlgProcW, _win32_DefDlgProc, _win32_defdlgproc_cpp, dlgbox.defdlgproc, winui._win32_defdlgproc, winuser/DefDlgProc, winuser/DefDlgProcW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DefDlgProcW (Unicode)
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
api_name:
 - DefDlgProc
 - DefDlgProcW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DefDlgProcW function


## -description


Calls the default dialog box window procedure to provide default processing for any window messages that a dialog box with a private window class does not process. 


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box. 


### -param Msg [in]

Type: <b>UINT</b>

The message. 


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



The <b>DefDlgProc</b> function is the window procedure for the predefined class of dialog box. This procedure provides internal processing for the dialog box by forwarding messages to the dialog box procedure and carrying out default processing for any messages that the dialog box procedure returns as <b>FALSE</b>. Applications that create custom window procedures for their custom dialog boxes often use <b>DefDlgProc</b> instead of the <a href="https://msdn.microsoft.com/en-us/library/ms633572(v=VS.85).aspx">DefWindowProc</a> function to carry out default message processing. 

Applications create custom dialog box classes by filling a <a href="https://msdn.microsoft.com/en-us/library/ms633576(v=VS.85).aspx">WNDCLASS</a> structure with appropriate information and registering the class with the <a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a> function. Some applications fill the structure by using the <a href="https://msdn.microsoft.com/en-us/library/ms633578(v=VS.85).aspx">GetClassInfo</a> function, specifying the name of the predefined dialog box. In such cases, the applications modify at least the <b>lpszClassName</b> member before registering. In all cases, the <b>cbWndExtra</b> member of <b>WNDCLASS</b> for a custom dialog box class must be set to at least <b>DLGWINDOWEXTRA</b>.

The <b>DefDlgProc</b> function must not be called by a dialog box procedure; doing so results in recursive execution. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633572(v=VS.85).aspx">DefWindowProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632588(v=VS.85).aspx">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633578(v=VS.85).aspx">GetClassInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633576(v=VS.85).aspx">WNDCLASS</a>
 

 

