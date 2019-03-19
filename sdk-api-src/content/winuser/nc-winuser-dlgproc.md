---
UID: NC:winuser.DLGPROC
title: DLGPROC (winuser.h)
author: windows-sdk-content
description: Application-defined callback function used with the CreateDialog and DialogBox families of functions.
old-location: dlgbox\dialogproc.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\dialogproc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DLGPROC, DLGPROC callback, DLGPROC callback function [Dialog Boxes], _win32_DialogProc, _win32_dialogproc_cpp, dlgbox.dialogproc, winui._win32_dialogproc, winuser/DLGPROC
ms.topic: callback
req.header: winuser.h
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
 - Winuser.h
api_name:
 - DLGPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DLGPROC callback function


## -description


Application-defined callback function used with the <a href="https://msdn.microsoft.com/en-us/library/ms645434(v=VS.85).aspx">CreateDialog</a> and <a href="https://msdn.microsoft.com/en-us/library/ms645452(v=VS.85).aspx">DialogBox</a> families of functions. It processes messages sent to a modal or modeless dialog box. The <b>DLGPROC</b> type defines a pointer to this callback function. <i>DialogProc</i> is a placeholder for the application-defined function name. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - hwndDlg [in]

Type: <b>HWND</b>

A handle to the dialog box. 


#### - lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information. 


#### - uMsg [in]

Type: <b>UINT</b>

The message. 


#### - wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information. 


## -returns



Type: <b>INT_PTR</b>

Typically, the dialog box procedure should return <b>TRUE</b> if it processed the message, and <b>FALSE</b> if it did not. If the dialog box procedure returns <b>FALSE</b>, the dialog manager performs the default dialog operation in response to the message.

If the dialog box procedure processes a message that requires a specific return value, the dialog box procedure should set the desired return value by calling <a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a>(<i>hwndDlg</i>, <b>DWL_MSGRESULT</b>, <i>lResult</i>) immediately before returning <b>TRUE</b>. Note that you must call <b>SetWindowLong</b> immediately before returning <b>TRUE</b>; doing so earlier may result in the <b>DWL_MSGRESULT</b> value being overwritten by a nested dialog box message.

The following messages are exceptions to the general rules stated above. Consult the documentation for the specific message for details on the semantics of the return value.

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb761358(v=VS.85).aspx">WM_CHARTOITEM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb775921(v=VS.85).aspx">WM_COMPAREITEM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb761849(v=VS.85).aspx">WM_CTLCOLORBTN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms645417(v=VS.85).aspx">WM_CTLCOLORDLG</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb761691(v=VS.85).aspx">WM_CTLCOLOREDIT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb761360(v=VS.85).aspx">WM_CTLCOLORLISTBOX</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb787573(v=VS.85).aspx">WM_CTLCOLORSCROLLBAR</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb787524(v=VS.85).aspx">WM_CTLCOLORSTATIC</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms632639(v=VS.85).aspx">WM_QUERYDRAGICON</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb761364(v=VS.85).aspx">WM_VKEYTOITEM</a>
</li>
</ul>



## -remarks



You should use the dialog box procedure only if you use the dialog box class for the dialog box. This is the default class and is used when no explicit class is specified in the dialog box template. Although the dialog box procedure is similar to a window procedure, it must not call the <a href="https://msdn.microsoft.com/en-us/library/ms633572(v=VS.85).aspx">DefWindowProc</a> function to process unwanted messages. Unwanted messages are processed internally by the dialog box window procedure. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645434(v=VS.85).aspx">CreateDialog</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645436(v=VS.85).aspx">CreateDialogIndirect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645441(v=VS.85).aspx">CreateDialogIndirectParam</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645445(v=VS.85).aspx">CreateDialogParam</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633572(v=VS.85).aspx">DefWindowProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632588(v=VS.85).aspx">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645452(v=VS.85).aspx">DialogBox</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645457(v=VS.85).aspx">DialogBoxIndirect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645461(v=VS.85).aspx">DialogBoxIndirectParam</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645465(v=VS.85).aspx">DialogBoxParam</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646312(v=VS.85).aspx">SetFocus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a>
 

 

