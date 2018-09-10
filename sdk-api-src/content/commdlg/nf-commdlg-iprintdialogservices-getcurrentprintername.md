---
UID: NF:commdlg.IPrintDialogServices.GetCurrentPrinterName
title: IPrintDialogServices::GetCurrentPrinterName
author: windows-sdk-content
description: Retrieves the name of the currently selected printer, for use with PrintDlgEx.
old-location: dlgbox\iprintdialogservices_getcurrentprintername.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogservices\iprintdialogservicesgetcurrentprintername.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetCurrentPrinterName, GetCurrentPrinterName function, GetCurrentPrinterName method [Dialog Boxes], GetCurrentPrinterName method [Dialog Boxes],IPrintDialogServices interface, IPrintDialogServices interface [Dialog Boxes],GetCurrentPrinterName method, IPrintDialogServices.GetCurrentPrinterName, IPrintDialogServices::GetCurrentPrinterName, _win32_IPrintDialogServices_GetCurrentPrinterName, _win32_iprintdialogservices_getcurrentprintername_cpp, commdlg/IPrintDialogServices::GetCurrentPrinterName, dlgbox.iprintdialogservices_getcurrentprintername, winui._win32_iprintdialogservices_getcurrentprintername
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: commdlg.h
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
req.dll: Comdlg32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comdlg32.dll
api_name:
 - IPrintDialogServices.GetCurrentPrinterName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrintDialogServices::GetCurrentPrinterName


## -description


Retrieves the name of the currently selected printer, for use with <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>.


## -parameters




### -param pPrinterName

Type: <b>LPTSTR</b>

The name of the currently selected printer.


### -param pcchSize

Type: <b>UINT*</b>

On input, the variable specifies the size, in characters, of the buffer pointed to by the <i>lpPrinterName</i> parameter. On output, the variable contains the number of bytes (ANSI) or characters (Unicode), including the terminating null character, written to the buffer.

                    

If the size is zero on input, the function returns the required buffer size (in bytes or characters) in <i>pcchSize</i> and does not use the <i>lpPrinterName</i> buffer.


## -returns



Type: <b>HRESULT</b>

If the method is successful, the return value is <b>S_OK</b>. If no printer is currently selected, the return value is <b>S_OK</b>, the value returned in <i>pcchSize</i> is zero, and the <i>lpPrinterName</i> buffer is unchanged.

                    

If an error occurs, the return value is a COM error code. For more information, see <a href="_com_error_handling">Error Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f8572f39-bccd-40ed-b556-3cac19920f15">IPrintDialogServices</a>



<a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>



<b>Reference</b>
 

 

