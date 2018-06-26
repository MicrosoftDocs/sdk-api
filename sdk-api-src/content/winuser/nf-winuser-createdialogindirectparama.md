---
UID: NF:winuser.CreateDialogIndirectParamA
title: CreateDialogIndirectParamA function
author: windows-sdk-content
description: Creates a modeless dialog box from a dialog box template in memory.
old-location: dlgbox\createdialogindirectparam.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\createdialogindirectparam.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CreateDialogIndirectParam, CreateDialogIndirectParam function [Dialog Boxes], CreateDialogIndirectParamA, CreateDialogIndirectParamW, _win32_CreateDialogIndirectParam, _win32_createdialogindirectparam_cpp, dlgbox.createdialogindirectparam, winui._win32_createdialogindirectparam, winuser/CreateDialogIndirectParam, winuser/CreateDialogIndirectParamA, winuser/CreateDialogIndirectParamW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateDialogIndirectParamW (Unicode) and CreateDialogIndirectParamA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-0.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - CreateDialogIndirectParam
 - CreateDialogIndirectParamA
 - CreateDialogIndirectParamW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CreateDialogIndirectParamA function


## -description


Creates a modeless dialog box from a dialog box template in memory. Before displaying the dialog box, the function passes an application-defined value to the dialog box procedure as the <i>lParam</i> parameter of the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message. An application can use this value to initialize dialog box controls.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module which contains the dialog box template. If this parameter is NULL, then the current executable is used.


### -param lpTemplate [in]

Type: <b>LPCDLGTEMPLATE</b>

The template <b>CreateDialogIndirectParam</b> uses to create the dialog box. A dialog box template consists of a header that describes the dialog box, followed by one or more additional blocks of data that describe each of the controls in the dialog box. The template can use either the standard format or the extended format. 
					

In a standard template, the header is a <a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a> structure followed by additional variable-length arrays. The data for each control consists of a <a href="https://msdn.microsoft.com/de214d1b-96d0-4e83-b848-2876d90bd629">DLGITEMTEMPLATE</a> structure followed by additional variable-length arrays. 

In an extended dialog box template, the header uses the <a href="https://msdn.microsoft.com/9f016cc6-56e2-45d3-8773-1b405fc10d29">DLGTEMPLATEEX</a> format and the control definitions use the <a href="https://msdn.microsoft.com/c60fd8db-ee4b-433b-a2fb-68b9a677bac8">DLGITEMTEMPLATEEX</a> format. 

After <b>CreateDialogIndirectParam</b> returns, you can free the template, which is only used to get the dialog box started. 


### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box. 


### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="https://msdn.microsoft.com/37c1b0b2-cf81-45d9-9a4e-9e5f7fa58dfd">DialogProc</a>. 


### -param dwInitParam

TBD




#### - lParamInit [in]

Type: <b>LPARAM</b>

The value to pass to the dialog box in the <i>lParam</i> parameter of the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message. 


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the window handle to the dialog box.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>CreateDialogIndirectParam</b> function uses the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function to create the dialog box. <b>CreateDialogIndirectParam</b> then sends a <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message to the dialog box procedure. If the template specifies the <a href="about_dialog_boxes.htm">DS_SETFONT</a> or DS_SHELLFONT style, the function also sends a <a href="https://msdn.microsoft.com/7db6b8af-dbec-4c29-8bf7-d7e95d9813c3">WM_SETFONT</a> message to the dialog box procedure. The function displays the dialog box if the template specifies the <b>WS_VISIBLE</b> style. Finally, <b>CreateDialogIndirectParam</b> returns the window handle to the dialog box. 

After <b>CreateDialogIndirectParam</b> returns, you can use the <a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a> function to display the dialog box (if it is not already visible). To destroy the dialog box, use the <a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a> function. To support keyboard navigation and other dialog box functionality, the message loop for the dialog box must call the <a href="https://msdn.microsoft.com/0afa23a3-f552-40f9-9713-e7bf790ba25c">IsDialogMessage</a> function.

In a standard dialog box template, the <a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a> structure and each of the <a href="https://msdn.microsoft.com/de214d1b-96d0-4e83-b848-2876d90bd629">DLGITEMTEMPLATE</a> structures must be aligned on <b>DWORD</b> boundaries. The creation data array that follows a <b>DLGITEMTEMPLATE</b> structure must also be aligned on a <b>DWORD</b> boundary. All of the other variable-length arrays in the template must be aligned on <b>WORD</b> boundaries. 

In an extended dialog box template, the <a href="https://msdn.microsoft.com/9f016cc6-56e2-45d3-8773-1b405fc10d29">DLGTEMPLATEEX</a> header and each of the <a href="https://msdn.microsoft.com/c60fd8db-ee4b-433b-a2fb-68b9a677bac8">DLGITEMTEMPLATEEX</a> control definitions must be aligned on <b>DWORD</b> boundaries. The creation data array, if any, that follows a <b>DLGITEMTEMPLATEEX</b> structure must also be aligned on a <b>DWORD</b> boundary. All of the other variable-length arrays in the template must be aligned on <b>WORD</b> boundaries. 

All character strings in the dialog box template, such as titles for the dialog box and buttons, must be Unicode strings.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9641daf4-2c38-49fb-b4fb-0e54491d095d">CreateDialog</a>



<a href="https://msdn.microsoft.com/b3bddf88-be6d-4aa3-9e23-257126bdfc15">CreateDialogIndirect</a>



<a href="https://msdn.microsoft.com/366d4035-d765-4600-87ca-5152c45f7fcd">CreateDialogParam</a>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/de214d1b-96d0-4e83-b848-2876d90bd629">DLGITEMTEMPLATE</a>



<a href="https://msdn.microsoft.com/c60fd8db-ee4b-433b-a2fb-68b9a677bac8">DLGITEMTEMPLATEEX</a>



<a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a>



<a href="https://msdn.microsoft.com/9f016cc6-56e2-45d3-8773-1b405fc10d29">DLGTEMPLATEEX</a>



<a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/37c1b0b2-cf81-45d9-9a4e-9e5f7fa58dfd">DialogProc</a>



<a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a>



<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>



<a href="https://msdn.microsoft.com/7db6b8af-dbec-4c29-8bf7-d7e95d9813c3">WM_SETFONT</a>
 

 

