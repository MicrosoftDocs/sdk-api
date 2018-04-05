---
UID: NF:winuser.CreateDialogW
title: CreateDialogW macro
author: windows-driver-content
description: Creates a modeless dialog box from a dialog box template resource. The CreateDialog macro uses the CreateDialogParam function.
old-location: dlgbox\createdialog.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\createdialog.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CreateDialog, CreateDialog function [Dialog Boxes], CreateDialogA, CreateDialogW, _win32_CreateDialog, _win32_createdialog_cpp, dlgbox.createdialog, winui._win32_createdialog, winuser/CreateDialog, winuser/CreateDialogA, winuser/CreateDialogW
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
req.unicode-ansi: CreateDialogW (Unicode) and CreateDialogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
api_name:
-	CreateDialog
-	CreateDialogA
-	CreateDialogW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CreateDialogW macro


## -description


Creates a modeless dialog box from a dialog box template resource. The <b>CreateDialog</b> macro uses the <a href="https://msdn.microsoft.com/366d4035-d765-4600-87ca-5152c45f7fcd">CreateDialogParam</a> function.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module which contains the dialog box template. If this parameter is NULL, then the current executable is used.


### -param lpName

TBD


### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box. 


### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="https://msdn.microsoft.com/37c1b0b2-cf81-45d9-9a4e-9e5f7fa58dfd">DialogProc</a>. 


#### - lpTemplate [in]

Type: <b>LPCTSTR</b>

The dialog box template. This parameter is either the pointer to a null-terminated character string that specifies the name of the dialog box template or an integer value that specifies the resource identifier of the dialog box template. If the parameter specifies a resource identifier, its high-order word must be zero and its low-order word must contain the identifier. You can use the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro to create this value. 


## -remarks



The <b>CreateDialog</b> function uses the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function to create the dialog box. <b>CreateDialog</b> then sends a <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message (and a <a href="https://msdn.microsoft.com/7db6b8af-dbec-4c29-8bf7-d7e95d9813c3">WM_SETFONT</a> message if the template specifies the <a href="about_dialog_boxes.htm">DS_SETFONT</a> or <b>DS_SHELLFONT</b> style) to the dialog box procedure. The function displays the dialog box if the template specifies the <b>WS_VISIBLE</b> style. Finally, <b>CreateDialog</b> returns the window handle to the dialog box. 

After <b>CreateDialog</b> returns, the application displays the dialog box (if it is not already displayed) by using the <a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a> function. The application destroys the dialog box by using the <a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a> function. To support keyboard navigation and other dialog box functionality, the message loop for the dialog box must call the <a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a> function.


#### Examples


			
			For an example, see <a href="using_dialog_boxes.htm">Creating a Modeless Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b3bddf88-be6d-4aa3-9e23-257126bdfc15">CreateDialogIndirect</a>



<a href="https://msdn.microsoft.com/f8ed581b-992e-41b8-a2f5-906b9bafa578">CreateDialogIndirectParam</a>



<a href="https://msdn.microsoft.com/366d4035-d765-4600-87ca-5152c45f7fcd">CreateDialogParam</a>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/0b28b084-e519-4114-9950-0aebf089b0c8">DialogBox</a>



<a href="https://msdn.microsoft.com/37c1b0b2-cf81-45d9-9a4e-9e5f7fa58dfd">DialogProc</a>



<a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a>



<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>



<a href="https://msdn.microsoft.com/7db6b8af-dbec-4c29-8bf7-d7e95d9813c3">WM_SETFONT</a>
 

 

