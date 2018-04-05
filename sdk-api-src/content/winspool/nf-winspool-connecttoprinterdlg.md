---
UID: NF:winspool.ConnectToPrinterDlg
title: ConnectToPrinterDlg function
author: windows-driver-content
description: The ConnectToPrinterDlg function displays a dialog box that lets users browse and connect to printers on a network.
old-location: gdi\connecttoprinterdlg.htm
old-project: printdocs
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ConnectToPrinterDlg, ConnectToPrinterDlg function [Windows GDI], _win32_ConnectToPrinterDlg, gdi.connecttoprinterdlg, winspool/ConnectToPrinterDlg
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
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
req.typenames: PRINT_EXECUTION_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WinSpool.drv
api_name:
-	ConnectToPrinterDlg
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: WinSpool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ConnectToPrinterDlg function


## -description


The <b>ConnectToPrinterDlg</b> function displays a dialog box that lets users browse and connect to printers on a network. If the user selects a printer, the function attempts to create a connection to it; if a suitable driver is not installed on the server, the user is given the option of creating a printer locally.


## -parameters




### -param hwnd [in]

Specifies the parent window of the dialog box.


### -param Flags [in]

This parameter is reserved and must be zero.


## -returns



If the function succeeds and the user selects a printer, the return value is a handle to the selected printer.

If the function fails, or the user cancels the dialog box without selecting a printer, the return value is <b>NULL</b>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <b>ConnectToPrinterDlg</b> function attempts to create a connection to the selected printer. However, if the server on which the printer resides does not have a suitable driver installed, the function offers the user the option of creating a printer locally. A calling application can determine whether the function has created a printer locally by calling <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a> with a <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure, then examining that structure's <b>Attributes</b> member.

An application should call <a href="https://msdn.microsoft.com/04d9c073-b795-4307-ba89-d4984bc5b354">DeletePrinter</a> to delete a local printer. An application should call <a href="https://msdn.microsoft.com/7b056eea-fbd9-4a08-a2dc-7326caeec387">DeletePrinterConnection</a> to delete a connection to a printer.




## -see-also




<a href="https://msdn.microsoft.com/6decf89a-1411-4e7e-aa20-60e7068658c2">AddPrinterConnection</a>



<a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a>



<a href="https://msdn.microsoft.com/04d9c073-b795-4307-ba89-d4984bc5b354">DeletePrinter</a>



<a href="https://msdn.microsoft.com/7b056eea-fbd9-4a08-a2dc-7326caeec387">DeletePrinterConnection</a>



<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

