---
UID: NF:winuser.DialogBoxW
title: DialogBoxW macro
author: windows-sdk-content
description: Creates a modal dialog box from a dialog box template resource. DialogBox does not return control until the specified callback function terminates the modal dialog box by calling the EndDialog function.
old-location: dlgbox\dialogbox.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\dialogbox.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DialogBox, DialogBox function [Dialog Boxes], DialogBoxA, DialogBoxW, _win32_DialogBox, _win32_dialogbox_cpp, dlgbox.dialogbox, winui._win32_dialogbox, winuser/DialogBox, winuser/DialogBoxA, winuser/DialogBoxW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DialogBoxW macro


## -description


Creates a modal dialog box from a dialog box template resource. <b>DialogBox</b> does not return control until the specified callback function terminates the modal dialog box by calling the <a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a> function.

<b>DialogBox</b> is implemented as a call to the <a href="https://msdn.microsoft.com/f6d6b80b-251f-44a0-9deb-e518af170b14">DialogBoxParam</a> function.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module which contains the dialog box template. If this parameter is NULL, then the current executable is used.


### -param lpTemplate [in]

Type: <b>LPCTSTR</b>

The dialog box template. This parameter is either the pointer to a null-terminated character string that specifies the name of the dialog box template or an integer value that specifies the resource identifier of the dialog box template. If the parameter specifies a resource identifier, its high-order word must be zero and its low-order word must contain the identifier. You can use the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro to create this value. 


### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box. 


### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="https://msdn.microsoft.com/37c1b0b2-cf81-45d9-9a4e-9e5f7fa58dfd">DialogProc</a>. 


## -remarks



The <b>DialogBox</b> macro uses the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function to create the dialog box. <b>DialogBox</b> then sends a <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message (and a <a href="https://msdn.microsoft.com/7db6b8af-dbec-4c29-8bf7-d7e95d9813c3">WM_SETFONT</a> message if the template specifies the <a href="about_dialog_boxes.htm">DS_SETFONT</a> or DS_SHELLFONT style) to the dialog box procedure. The function displays the dialog box (regardless of whether the template specifies the <b>WS_VISIBLE</b> style), disables the owner window, and starts its own message loop to retrieve and dispatch messages for the dialog box. 

When the dialog box procedure calls the <a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a> function, <b>DialogBox</b> destroys the dialog box, ends the message loop, enables the owner window (if previously enabled), and returns the <i>nResult</i> parameter specified by the dialog box procedure when it called <b>EndDialog</b>. 


#### Examples

For an example, see <a href="using_dialog_boxes.htm">Creating a Modal Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9641daf4-2c38-49fb-b4fb-0e54491d095d">CreateDialog</a>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/0af783b3-804d-4075-8046-5109f37e275d">DialogBoxIndirect</a>



<a href="https://msdn.microsoft.com/ce241d7b-8775-4c0d-bb4b-87df5f58f8a8">DialogBoxIndirectParam</a>



<a href="https://msdn.microsoft.com/f6d6b80b-251f-44a0-9deb-e518af170b14">DialogBoxParam</a>



<a href="https://msdn.microsoft.com/37c1b0b2-cf81-45d9-9a4e-9e5f7fa58dfd">DialogProc</a>



<a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>



<a href="https://msdn.microsoft.com/7db6b8af-dbec-4c29-8bf7-d7e95d9813c3">WM_SETFONT</a>
 

 

