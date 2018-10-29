---
UID: NF:winuser.CreateDialogA
title: CreateDialogA macro
author: windows-sdk-content
description: Creates a modeless dialog box from a dialog box template resource. The CreateDialog macro uses the CreateDialogParam function.
old-location: dlgbox\createdialog.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\createdialog.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
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
 - CreateDialog
 - CreateDialogA
 - CreateDialogW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateDialogA macro


## -description


Creates a modeless dialog box from a dialog box template resource. The <b>CreateDialog</b> macro uses the <a href="https://msdn.microsoft.com/en-us/library/ms645445(v=VS.85).aspx">CreateDialogParam</a> function.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module which contains the dialog box template. If this parameter is NULL, then the current executable is used.


### -param lpName [in]

Type: <b>LPCTSTR</b>

The dialog box template. This parameter is either the pointer to a null-terminated character string that specifies the name of the dialog box template or an integer value that specifies the resource identifier of the dialog box template. If the parameter specifies a resource identifier, its high-order word must be zero and its low-order word must contain the identifier. You can use the <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a> macro to create this value. 


### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box. 


### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="https://msdn.microsoft.com/en-us/library/ms645469(v=VS.85).aspx">DialogProc</a>. 


## -remarks



The <b>CreateDialog</b> function uses the <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> function to create the dialog box. <b>CreateDialog</b> then sends a <a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a> message (and a <a href="https://msdn.microsoft.com/en-us/library/ms632642(v=VS.85).aspx">WM_SETFONT</a> message if the template specifies the <a href="https://msdn.microsoft.com/en-us/library/ms644994(v=VS.85).aspx">DS_SETFONT</a> or <b>DS_SHELLFONT</b> style) to the dialog box procedure. The function displays the dialog box if the template specifies the <b>WS_VISIBLE</b> style. Finally, <b>CreateDialog</b> returns the window handle to the dialog box. 

After <b>CreateDialog</b> returns, the application displays the dialog box (if it is not already displayed) by using the <a href="https://msdn.microsoft.com/en-us/library/ms633548(v=VS.85).aspx">ShowWindow</a> function. The application destroys the dialog box by using the <a href="https://msdn.microsoft.com/en-us/library/ms632682(v=VS.85).aspx">DestroyWindow</a> function. To support keyboard navigation and other dialog box functionality, the message loop for the dialog box must call the <a href="https://msdn.microsoft.com/en-us/library/ms645498(v=VS.85).aspx">IsDialogMessage</a> function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms644996(v=VS.85).aspx">Creating a Modeless Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645436(v=VS.85).aspx">CreateDialogIndirect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645441(v=VS.85).aspx">CreateDialogIndirectParam</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645445(v=VS.85).aspx">CreateDialogParam</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632682(v=VS.85).aspx">DestroyWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632588(v=VS.85).aspx">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645452(v=VS.85).aspx">DialogBox</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645469(v=VS.85).aspx">DialogProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645498(v=VS.85).aspx">IsDialogMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633548(v=VS.85).aspx">ShowWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645428(v=VS.85).aspx">WM_INITDIALOG</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632642(v=VS.85).aspx">WM_SETFONT</a>
 

 

