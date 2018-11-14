---
UID: NF:winuser.DialogBoxIndirectA
title: DialogBoxIndirectA macro
author: windows-sdk-content
description: Creates a modal dialog box from a dialog box template in memory. DialogBoxIndirect does not return control until the specified callback function terminates the modal dialog box by calling the EndDialog function.
old-location: dlgbox\dialogboxindirect.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\dialogboxindirect.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DialogBoxIndirect, DialogBoxIndirect function [Dialog Boxes], DialogBoxIndirectA, DialogBoxIndirectW, _win32_DialogBoxIndirect, _win32_dialogboxindirect_cpp, dlgbox.dialogboxindirect, winui._win32_dialogboxindirect, winuser/DialogBoxIndirect, winuser/DialogBoxIndirectA, winuser/DialogBoxIndirectW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DialogBoxIndirectW (Unicode) and DialogBoxIndirectA (ANSI)
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
 - DialogBoxIndirect
 - DialogBoxIndirectA
 - DialogBoxIndirectW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- winuser.h
: 
- DialogBoxIndirectA
: 
---

# DialogBoxIndirectA macro


## -description


Creates a modal dialog box from a dialog box template in memory. <b>DialogBoxIndirect</b> does not return control until the specified callback function terminates the modal dialog box by calling the <a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a> function.

<b>DialogBoxIndirect</b> is implemented as a call to the <a href="https://msdn.microsoft.com/ce241d7b-8775-4c0d-bb4b-87df5f58f8a8">DialogBoxIndirectParam</a> function.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module that creates the dialog box. 


### -param lpTemplate [in]

Type: <b>LPCDLGTEMPLATE</b>

The template that <b>DialogBoxIndirect</b> uses to create the dialog box. A dialog box template consists of a header that describes the dialog box, followed by one or more additional blocks of data that describe each of the controls in the dialog box. The template can use either the standard format or the extended format. 
					

In a standard template for a dialog box, the header is a <a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a> structure followed by additional variable-length arrays. The data for each control consists of a <a href="https://msdn.microsoft.com/de214d1b-96d0-4e83-b848-2876d90bd629">DLGITEMTEMPLATE</a> structure followed by additional variable-length arrays. 

In an extended template for a dialog box, the header uses the <a href="https://msdn.microsoft.com/9f016cc6-56e2-45d3-8773-1b405fc10d29">DLGTEMPLATEEX</a> format and the control definitions use the <a href="https://msdn.microsoft.com/c60fd8db-ee4b-433b-a2fb-68b9a677bac8">DLGITEMTEMPLATEEX</a> format. 


### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box. 


### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="https://msdn.microsoft.com/37c1b0b2-cf81-45d9-9a4e-9e5f7fa58dfd">DialogProc</a>. 


## -remarks



The <b>DialogBoxIndirect</b> macro uses the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function to create the dialog box. <b>DialogBoxIndirect</b> then sends a <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message to the dialog box procedure. If the template specifies the <a href="about_dialog_boxes.htm">DS_SETFONT</a> or DS_SHELLFONT style, the function also sends a <a href="https://msdn.microsoft.com/7db6b8af-dbec-4c29-8bf7-d7e95d9813c3">WM_SETFONT</a> message to the dialog box procedure. The function displays the dialog box (regardless of whether the template specifies the <b>WS_VISIBLE</b> style), disables the owner window, and starts its own message loop to retrieve and dispatch messages for the dialog box. 

When the dialog box procedure calls the <a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a> function, <b>DialogBoxIndirect</b> destroys the dialog box, ends the message loop, enables the owner window (if previously enabled), and returns the <i>nResult</i> parameter specified by the dialog box procedure when it called <b>EndDialog</b>. 

In a standard dialog box template, the <a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a> structure and each of the <a href="https://msdn.microsoft.com/de214d1b-96d0-4e83-b848-2876d90bd629">DLGITEMTEMPLATE</a> structures must be aligned on <b>DWORD</b> boundaries. The creation data array that follows a <b>DLGITEMTEMPLATE</b> structure must also be aligned on a <b>DWORD</b> boundary. All of the other variable-length arrays in the template must be aligned on <b>WORD</b> boundaries. 

In an extended dialog box template, the <a href="https://msdn.microsoft.com/9f016cc6-56e2-45d3-8773-1b405fc10d29">DLGTEMPLATEEX</a> header and each of the <a href="https://msdn.microsoft.com/c60fd8db-ee4b-433b-a2fb-68b9a677bac8">DLGITEMTEMPLATEEX</a> control definitions must be aligned on <b>DWORD</b> boundaries. The creation data array, if any, that follows a <b>DLGITEMTEMPLATEEX</b> structure must also be aligned on a <b>DWORD</b> boundary. All of the other variable-length arrays in the template must be aligned on <b>WORD</b> boundaries. 

All character strings in the dialog box template, such as titles for the dialog box and buttons, must be Unicode strings. Use the <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> function to generate Unicode strings from ANSI strings.


#### Examples

For an example, see <a href="using_dialog_boxes.htm">Creating a Template in Memory</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/de214d1b-96d0-4e83-b848-2876d90bd629">DLGITEMTEMPLATE</a>



<a href="https://msdn.microsoft.com/c60fd8db-ee4b-433b-a2fb-68b9a677bac8">DLGITEMTEMPLATEEX</a>



<a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a>



<a href="https://msdn.microsoft.com/9f016cc6-56e2-45d3-8773-1b405fc10d29">DLGTEMPLATEEX</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/0b28b084-e519-4114-9950-0aebf089b0c8">DialogBox</a>



<a href="https://msdn.microsoft.com/ce241d7b-8775-4c0d-bb4b-87df5f58f8a8">DialogBoxIndirectParam</a>



<a href="https://msdn.microsoft.com/f6d6b80b-251f-44a0-9deb-e518af170b14">DialogBoxParam</a>



<a href="https://msdn.microsoft.com/37c1b0b2-cf81-45d9-9a4e-9e5f7fa58dfd">DialogProc</a>



<a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a>



<a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>



<a href="https://msdn.microsoft.com/7db6b8af-dbec-4c29-8bf7-d7e95d9813c3">WM_SETFONT</a>
 

 

