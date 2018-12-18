---
UID: NF:commdlg.IPrintDialogServices.GetCurrentPrinterName
title: IPrintDialogServices::GetCurrentPrinterName
author: windows-sdk-content
description: Retrieves the name of the currently selected printer, for use with PrintDlgEx.
old-location: dlgbox\iprintdialogservices_getcurrentprintername.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogservices\iprintdialogservicesgetcurrentprintername.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrentPrinterName, GetCurrentPrinterName function, GetCurrentPrinterName method [Dialog Boxes], GetCurrentPrinterName method [Dialog Boxes],IPrintDialogServices interface, IPrintDialogServices interface [Dialog Boxes],GetCurrentPrinterName method, IPrintDialogServices.GetCurrentPrinterName, IPrintDialogServices::GetCurrentPrinterName, _win32_IPrintDialogServices_GetCurrentPrinterName, _win32_iprintdialogservices_getcurrentprintername_cpp, commdlg/IPrintDialogServices::GetCurrentPrinterName, dlgbox.iprintdialogservices_getcurrentprintername, winui._win32_iprintdialogservices_getcurrentprintername
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


Retrieves the name of the currently selected printer, for use with <a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a>.


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

                    

If an error occurs, the return value is a COM error code. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa376932(v=VS.85).aspx">Error Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms645524(v=VS.85).aspx">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646897(v=VS.85).aspx">IPrintDialogServices</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a>



<b>Reference</b>
 

 

