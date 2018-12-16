---
UID: NF:winuser.DialogBoxA
title: DialogBoxA macro
author: windows-sdk-content
description: Creates a modal dialog box from a dialog box template resource. DialogBox does not return control until the specified callback function terminates the modal dialog box by calling the EndDialog function.
old-location: dlgbox\dialogbox.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\dialogbox.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DialogBox, DialogBox function [Dialog Boxes], DialogBoxA, DialogBoxW, _win32_DialogBox, _win32_dialogbox_cpp, dlgbox.dialogbox, winui._win32_dialogbox, winuser/DialogBox, winuser/DialogBoxA, winuser/DialogBoxW
ms.topic: macro
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DialogBoxW (Unicode) and DialogBoxA (ANSI)
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
 - DialogBox
 - DialogBoxA
 - DialogBoxW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DialogBoxA macro


## -description


Creates a modal dialog box from a dialog box template resource. <b>DialogBox</b> does not return control until the specified callback function terminates the modal dialog box by calling the <a href="https://msdn.microsoft.com/en-us/library/ms645472(v=VS.85).aspx">EndDialog</a> function.

<b>DialogBox</b> is implemented as a call to the <a href="https://msdn.microsoft.com/en-us/library/ms645465(v=VS.85).aspx">DialogBoxParam</a> function.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module which contains the dialog box template. If this parameter is NULL, then the current executable is used.


### -param lpTemplate [in]

Type: <b>LPCTSTR</b>

The dialog box template. This parameter is either the pointer to a null-terminated character string that specifies the name of the dialog box template or an integer value that specifies the resource identifier of the dialog box template. If the parameter specifies a resource identifier, its high-order word must be zero and its low-order word must contain the identifier. You can use the <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a> macro to create this value. 


### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box. 


### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="https://msdn.microsoft.com/en-us/library/ms645469(v=VS.85).aspx">DialogProc</a>. 


## -remarks



The <b>DialogBox</b> macro uses the <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> function to create the dialog box. <b>DialogBox</b> then sends a <a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a> message (and a <a href="https://msdn.microsoft.com/en-us/library/ms632642(v=VS.85).aspx">WM_SETFONT</a> message if the template specifies the <a href="https://msdn.microsoft.com/en-us/library/ms644994(v=VS.85).aspx">DS_SETFONT</a> or DS_SHELLFONT style) to the dialog box procedure. The function displays the dialog box (regardless of whether the template specifies the <b>WS_VISIBLE</b> style), disables the owner window, and starts its own message loop to retrieve and dispatch messages for the dialog box. 

When the dialog box procedure calls the <a href="https://msdn.microsoft.com/en-us/library/ms645472(v=VS.85).aspx">EndDialog</a> function, <b>DialogBox</b> destroys the dialog box, ends the message loop, enables the owner window (if previously enabled), and returns the <i>nResult</i> parameter specified by the dialog box procedure when it called <b>EndDialog</b>. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644996(v=VS.85).aspx">Creating a Modal Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645434(v=VS.85).aspx">CreateDialog</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632588(v=VS.85).aspx">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645457(v=VS.85).aspx">DialogBoxIndirect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645461(v=VS.85).aspx">DialogBoxIndirectParam</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645465(v=VS.85).aspx">DialogBoxParam</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645469(v=VS.85).aspx">DialogProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645472(v=VS.85).aspx">EndDialog</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632642(v=VS.85).aspx">WM_SETFONT</a>
 

 

