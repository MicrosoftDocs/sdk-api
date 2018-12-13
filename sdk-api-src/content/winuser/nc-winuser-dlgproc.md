---
UID: NC:winuser.DLGPROC
title: DLGPROC
author: windows-sdk-content
description: Application-defined callback function used with the CreateDialog and DialogBox families of functions.
old-location: dlgbox\dialogproc.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\dialogproc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DLGPROC, DLGPROC callback, DLGPROC callback function [Dialog Boxes], _win32_DialogProc, _win32_dialogproc_cpp, dlgbox.dialogproc, winui._win32_dialogproc, winuser/DLGPROC
ms.prod: windows-hardware
ms.technology: windows-devices
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


Application-defined callback function used with the <a href="https://msdn.microsoft.com/9641daf4-2c38-49fb-b4fb-0e54491d095d">CreateDialog</a> and <a href="https://msdn.microsoft.com/0b28b084-e519-4114-9950-0aebf089b0c8">DialogBox</a> families of functions. It processes messages sent to a modal or modeless dialog box. The <b>DLGPROC</b> type defines a pointer to this callback function. <i>DialogProc</i> is a placeholder for the application-defined function name. 


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

If the dialog box procedure processes a message that requires a specific return value, the dialog box procedure should set the desired return value by calling <a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a>(<i>hwndDlg</i>, <b>DWL_MSGRESULT</b>, <i>lResult</i>) immediately before returning <b>TRUE</b>. Note that you must call <b>SetWindowLong</b> immediately before returning <b>TRUE</b>; doing so earlier may result in the <b>DWL_MSGRESULT</b> value being overwritten by a nested dialog box message.

The following messages are exceptions to the general rules stated above. Consult the documentation for the specific message for details on the semantics of the return value.

<ul>
<li>
<a href="_win32_WM_CHARTOITEM">WM_CHARTOITEM</a>
</li>
<li>
<a href="_win32_WM_COMPAREITEM">WM_COMPAREITEM</a>
</li>
<li>
<a href="_win32_WM_CTLCOLORBTN">WM_CTLCOLORBTN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5b90ab3f-b751-486f-a0fa-33f791c31a26">WM_CTLCOLORDLG</a>
</li>
<li>
<a href="_win32_WM_CTLCOLOREDIT">WM_CTLCOLOREDIT</a>
</li>
<li>
<a href="_win32_WM_CTLCOLORLISTBOX">WM_CTLCOLORLISTBOX</a>
</li>
<li>
<a href="_win32_WM_CTLCOLORSCROLLBAR">WM_CTLCOLORSCROLLBAR</a>
</li>
<li>
<a href="_win32_WM_CTLCOLORSTATIC">WM_CTLCOLORSTATIC</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e4f0e638-f606-4745-888b-14a846c7fd37">WM_QUERYDRAGICON</a>
</li>
<li>
<a href="_win32_WM_VKEYTOITEM">WM_VKEYTOITEM</a>
</li>
</ul>



## -remarks



You should use the dialog box procedure only if you use the dialog box class for the dialog box. This is the default class and is used when no explicit class is specified in the dialog box template. Although the dialog box procedure is similar to a window procedure, it must not call the <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> function to process unwanted messages. Unwanted messages are processed internally by the dialog box window procedure. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9641daf4-2c38-49fb-b4fb-0e54491d095d">CreateDialog</a>



<a href="https://msdn.microsoft.com/b3bddf88-be6d-4aa3-9e23-257126bdfc15">CreateDialogIndirect</a>



<a href="https://msdn.microsoft.com/f8ed581b-992e-41b8-a2f5-906b9bafa578">CreateDialogIndirectParam</a>



<a href="https://msdn.microsoft.com/366d4035-d765-4600-87ca-5152c45f7fcd">CreateDialogParam</a>



<a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/0b28b084-e519-4114-9950-0aebf089b0c8">DialogBox</a>



<a href="https://msdn.microsoft.com/0af783b3-804d-4075-8046-5109f37e275d">DialogBoxIndirect</a>



<a href="https://msdn.microsoft.com/ce241d7b-8775-4c0d-bb4b-87df5f58f8a8">DialogBoxIndirectParam</a>



<a href="https://msdn.microsoft.com/f6d6b80b-251f-44a0-9deb-e518af170b14">DialogBoxParam</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/88fc2959-007a-441d-8a02-19d775f28de9">SetFocus</a>



<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>
 

 

