---
UID: NF:winuser.CreateDialogIndirectW
title: CreateDialogIndirectW macro
author: windows-sdk-content
description: Creates a modeless dialog box from a dialog box template in memory. The CreateDialogIndirect macro uses the CreateDialogIndirectParam function.
old-location: dlgbox\createdialogindirect.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\createdialogindirect.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateDialogIndirect, CreateDialogIndirect function [Dialog Boxes], CreateDialogIndirectA, CreateDialogIndirectW, _win32_CreateDialogIndirect, _win32_createdialogindirect_cpp, dlgbox.createdialogindirect, winui._win32_createdialogindirect, winuser/CreateDialogIndirect, winuser/CreateDialogIndirectA, winuser/CreateDialogIndirectW
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
req.unicode-ansi: CreateDialogIndirectW (Unicode) and CreateDialogIndirectA (ANSI)
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
 - CreateDialogIndirect
 - CreateDialogIndirectA
 - CreateDialogIndirectW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateDialogIndirectW macro


## -description


Creates a modeless dialog box from a dialog box template in memory. The <b>CreateDialogIndirect</b> macro uses the <a href="https://msdn.microsoft.com/en-us/library/ms645441(v=VS.85).aspx">CreateDialogIndirectParam</a> function.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module that creates the dialog box.


### -param lpTemplate [in]

Type: <b>LPCDLGTEMPLATE</b>

A template that <b>CreateDialogIndirect</b> uses to create the dialog box. A dialog box template consists of a header that describes the dialog box, followed by one or more additional blocks of data that describe each of the controls in the dialog box. The template can use either the standard format or the extended format. 
					

In a standard template, the header is a <a href="https://msdn.microsoft.com/en-us/library/ms645394(v=VS.85).aspx">DLGTEMPLATE</a> structure followed by additional variable-length arrays. The data for each control consists of a <a href="https://msdn.microsoft.com/en-us/library/ms644997(v=VS.85).aspx">DLGITEMTEMPLATE</a> structure followed by additional variable-length arrays.

In an extended dialog box template, the header uses the <a href="https://msdn.microsoft.com/en-us/library/ms645398(v=VS.85).aspx">DLGTEMPLATEEX</a> format and the control definitions use the <a href="https://msdn.microsoft.com/en-us/library/ms645389(v=VS.85).aspx">DLGITEMTEMPLATEEX</a> format.

After <b>CreateDialogIndirect</b> returns, you can free the template, which is only used to get the dialog box started. 


### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box.


### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="https://msdn.microsoft.com/en-us/library/ms645469(v=VS.85).aspx">DialogProc</a>. 


## -remarks



The <b>CreateDialogIndirect</b> macro uses the <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> function to create the dialog box. <b>CreateDialogIndirect</b> then sends a <a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a> message to the dialog box procedure. If the template specifies the <a href="https://msdn.microsoft.com/en-us/library/ms644994(v=VS.85).aspx">DS_SETFONT</a> or DS_SHELLFONT style, the function also sends a <a href="https://msdn.microsoft.com/en-us/library/ms632642(v=VS.85).aspx">WM_SETFONT</a> message to the dialog box procedure. The function displays the dialog box if the template specifies the WS_VISIBLE style. Finally, <b>CreateDialogIndirect</b> returns the window handle to the dialog box. 

After <b>CreateDialogIndirect</b> returns, you can use the <a href="https://msdn.microsoft.com/en-us/library/ms633548(v=VS.85).aspx">ShowWindow</a> function to display the dialog box (if it is not already visible). To destroy the dialog box, use the <a href="https://msdn.microsoft.com/en-us/library/ms632682(v=VS.85).aspx">DestroyWindow</a> function. To support keyboard navigation and other dialog box functionality, the message loop for the dialog box must call the <a href="https://msdn.microsoft.com/en-us/library/ms645498(v=VS.85).aspx">IsDialogMessage</a> function.

In a standard dialog box template, the <a href="https://msdn.microsoft.com/en-us/library/ms645394(v=VS.85).aspx">DLGTEMPLATE</a> structure and each of the <a href="https://msdn.microsoft.com/en-us/library/ms644997(v=VS.85).aspx">DLGITEMTEMPLATE</a> structures must be aligned on <b>DWORD</b> boundaries. The creation data array that follows a <b>DLGITEMTEMPLATE</b> structure must also be aligned on a <b>DWORD</b> boundary. All of the other variable-length arrays in the template must be aligned on <b>WORD</b> boundaries. 

In an extended dialog box template, the <a href="https://msdn.microsoft.com/en-us/library/ms645398(v=VS.85).aspx">DLGTEMPLATEEX</a> header and each of the <a href="https://msdn.microsoft.com/en-us/library/ms645389(v=VS.85).aspx">DLGITEMTEMPLATEEX</a> control definitions must be aligned on <b>DWORD</b> boundaries. The creation data array, if any, that follows a <b>DLGITEMTEMPLATEEX</b> structure must also be aligned on a <b>DWORD</b> boundary. All of the other variable-length arrays in the template must be aligned on <b>WORD</b> boundaries. 

All character strings in the dialog box template, such as titles for the dialog box and buttons, must be Unicode strings. Use the <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> function to generate Unicode strings from ANSI strings.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645434(v=VS.85).aspx">CreateDialog</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645441(v=VS.85).aspx">CreateDialogIndirectParam</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645445(v=VS.85).aspx">CreateDialogParam</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644997(v=VS.85).aspx">DLGITEMTEMPLATE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645389(v=VS.85).aspx">DLGITEMTEMPLATEEX</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645394(v=VS.85).aspx">DLGTEMPLATE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645398(v=VS.85).aspx">DLGTEMPLATEEX</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632682(v=VS.85).aspx">DestroyWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632588(v=VS.85).aspx">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645469(v=VS.85).aspx">DialogProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645498(v=VS.85).aspx">IsDialogMessage</a>



<a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633548(v=VS.85).aspx">ShowWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632642(v=VS.85).aspx">WM_SETFONT</a>
 

 

