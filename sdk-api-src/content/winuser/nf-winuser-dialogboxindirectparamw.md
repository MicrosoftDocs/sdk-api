---
UID: NF:winuser.DialogBoxIndirectParamW
title: DialogBoxIndirectParamW function
author: windows-sdk-content
description: Creates a modal dialog box from a dialog box template in memory.
old-location: dlgbox\dialogboxindirectparam.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\dialogboxindirectparam.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: DialogBoxIndirectParam, DialogBoxIndirectParam function [Dialog Boxes], DialogBoxIndirectParamA, DialogBoxIndirectParamW, _win32_DialogBoxIndirectParam, _win32_dialogboxindirectparam_cpp, dlgbox.dialogboxindirectparam, winui._win32_dialogboxindirectparam, winuser/DialogBoxIndirectParam, winuser/DialogBoxIndirectParamA, winuser/DialogBoxIndirectParamW
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
req.unicode-ansi: DialogBoxIndirectParamW (Unicode) and DialogBoxIndirectParamA (ANSI)
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
 - Ext-MS-Win-NTUser-DialogBox-l1-1-0.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - DialogBoxIndirectParam
 - DialogBoxIndirectParamA
 - DialogBoxIndirectParamW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DialogBoxIndirectParamW function


## -description


Creates a modal dialog box from a dialog box template in memory. Before displaying the dialog box, the function passes an application-defined value to the dialog box procedure as the <i>lParam</i> parameter of the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message. An application can use this value to initialize dialog box controls. 


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module that creates the dialog box. 


### -param hDialogTemplate [in]

Type: <b>LPCDLGTEMPLATE</b>

The template that <b>DialogBoxIndirectParam</b> uses to create the dialog box. A dialog box template consists of a header that describes the dialog box, followed by one or more additional blocks of data that describe each of the controls in the dialog box. The template can use either the standard format or the extended format. 
					

In a standard template for a dialog box, the header is a <a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a> structure followed by additional variable-length arrays. The data for each control consists of a <a href="https://msdn.microsoft.com/de214d1b-96d0-4e83-b848-2876d90bd629">DLGITEMTEMPLATE</a> structure followed by additional variable-length arrays. 

In an extended template for a dialog box, the header uses the <a href="https://msdn.microsoft.com/9f016cc6-56e2-45d3-8773-1b405fc10d29">DLGTEMPLATEEX</a> format and the control definitions use the <a href="https://msdn.microsoft.com/c60fd8db-ee4b-433b-a2fb-68b9a677bac8">DLGITEMTEMPLATEEX</a> format. 


### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box. 


### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="https://msdn.microsoft.com/37c1b0b2-cf81-45d9-9a4e-9e5f7fa58dfd">DialogProc</a>. 


### -param dwInitParam [in]

Type: <b>LPARAM</b>

The value to pass to the dialog box in the <i>lParam</i> parameter of the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message. 


## -returns



Type: <b>INT_PTR</b>

If the function succeeds, the return value is the <i>nResult</i> parameter specified in the call to the <a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a> function that was used to terminate the dialog box.

If the function fails because the <i>hWndParent</i> parameter is invalid, the return value is zero. The function returns zero in this case for compatibility with previous versions of Windows. If the function fails for any other reason, the return value is –1. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>DialogBoxIndirectParam</b> function uses the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function to create the dialog box. <b>DialogBoxIndirectParam</b> then sends a <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message to the dialog box procedure. If the template specifies the <a href="about_dialog_boxes.htm">DS_SETFONT</a> or DS_SHELLFONT style, the function also sends a <a href="https://msdn.microsoft.com/7db6b8af-dbec-4c29-8bf7-d7e95d9813c3">WM_SETFONT</a> message to the dialog box procedure. The function displays the dialog box (regardless of whether the template specifies the <b>WS_VISIBLE</b> style), disables the owner window, and starts its own message loop to retrieve and dispatch messages for the dialog box. 

When the dialog box procedure calls the <a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a> function, <b>DialogBoxIndirectParam</b> destroys the dialog box, ends the message loop, enables the owner window (if previously enabled), and returns the <i>nResult</i> parameter specified by the dialog box procedure when it called <b>EndDialog</b>. 

In a standard dialog box template, the <a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a> structure and each of the <a href="https://msdn.microsoft.com/de214d1b-96d0-4e83-b848-2876d90bd629">DLGITEMTEMPLATE</a> structures must be aligned on <b>DWORD</b> boundaries. The creation data array that follows a <b>DLGITEMTEMPLATE</b> structure must also be aligned on a <b>DWORD</b> boundary. All of the other variable-length arrays in the template must be aligned on <b>WORD</b> boundaries. 

In an extended dialog box template, the <a href="https://msdn.microsoft.com/9f016cc6-56e2-45d3-8773-1b405fc10d29">DLGTEMPLATEEX</a> header and each of the <a href="https://msdn.microsoft.com/c60fd8db-ee4b-433b-a2fb-68b9a677bac8">DLGITEMTEMPLATEEX</a> control definitions must be aligned on <b>DWORD</b> boundaries. The creation data array, if any, that follows a <b>DLGITEMTEMPLATEEX</b> structure must also be aligned on a <b>DWORD</b> boundary. All of the other variable-length arrays in the template must be aligned on <b>WORD</b> boundaries. 

All character strings in the dialog box template, such as titles for the dialog box and buttons, must be Unicode strings.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/de214d1b-96d0-4e83-b848-2876d90bd629">DLGITEMTEMPLATE</a>



<a href="https://msdn.microsoft.com/c60fd8db-ee4b-433b-a2fb-68b9a677bac8">DLGITEMTEMPLATEEX</a>



<a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a>



<a href="https://msdn.microsoft.com/9f016cc6-56e2-45d3-8773-1b405fc10d29">DLGTEMPLATEEX</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/0b28b084-e519-4114-9950-0aebf089b0c8">DialogBox</a>



<a href="https://msdn.microsoft.com/0af783b3-804d-4075-8046-5109f37e275d">DialogBoxIndirect</a>



<a href="https://msdn.microsoft.com/f6d6b80b-251f-44a0-9deb-e518af170b14">DialogBoxParam</a>



<a href="https://msdn.microsoft.com/37c1b0b2-cf81-45d9-9a4e-9e5f7fa58dfd">DialogProc</a>



<a href="https://msdn.microsoft.com/925e8aa8-9d8d-4bec-a19e-ba24e78b2d10">EndDialog</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>



<a href="https://msdn.microsoft.com/7db6b8af-dbec-4c29-8bf7-d7e95d9813c3">WM_SETFONT</a>
 

 

