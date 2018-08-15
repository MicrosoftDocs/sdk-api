---
UID: NF:commdlg.GetCurrentDevMode
title: GetCurrentDevMode function
author: windows-sdk-content
description: Fills a DEVMODE structure with information about the currently selected printer for use with PrintDlgEx.
old-location: dlgbox\iprintdialogservices_getcurrentdevmode.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogservices\iprintdialogservicesgetcurrentdevmode.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetCurrentDevMode, GetCurrentDevMode function, GetCurrentDevMode method [Dialog Boxes], GetCurrentDevMode method [Dialog Boxes],IPrintDialogServices interface, IPrintDialogServices interface [Dialog Boxes],GetCurrentDevMode method, IPrintDialogServices::GetCurrentDevMode, _win32_IPrintDialogServices_GetCurrentDevMode, _win32_iprintdialogservices_getcurrentdevmode_cpp, commdlg/IPrintDialogServices::GetCurrentDevMode, dlgbox.iprintdialogservices_getcurrentdevmode, winui._win32_iprintdialogservices_getcurrentdevmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: commdlg.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: UDACCEL, *LPUDACCEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comdlg32.dll
api_name:
 - IPrintDialogServices.GetCurrentDevMode
product: Windows
targetos: Windows
req.lib: 
req.dll: Comdlg32.dll
req.irql: 
---

# GetCurrentDevMode function


## -description


Fills a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure with information about the currently selected printer for use with <a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a>.


## -parameters




### -param pDevMode

Type: <b>LPDEVMODE</b>

A pointer to a buffer that receives a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure containing information about the currently selected printer.


### -param pcbSize

Type: <b>UINT*</b>

On input, the variable specifies the size, in bytes, of the buffer pointed to by the <i>lpDevMode</i> parameter. On output, the variable contains the number of bytes written to <i>lpDevMode</i>.

If the size is zero on input, the function returns the required buffer size (in bytes) in <i>pcbSize</i> and does not use the <i>lpDevMode</i> buffer.


## -returns



Type: <b>HRESULT</b>

If the method is successful, the return value is <b>S_OK</b>. If no printer is currently selected, the return value is <b>S_OK</b>, the value returned in <i>pcbSize</i> is zero, and the <i>lpDevMode</i> buffer is unchanged.

If an error occurs, the return value is a COM error code. For more information, see <a href="_com_error_handling">Error Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms645524(v=VS.85).aspx">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646897(v=VS.85).aspx">IPrintDialogServices</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a>



<b>Reference</b>
 

 

