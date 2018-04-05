---
UID: NF:winspool.AdvancedDocumentPropertiesA
title: AdvancedDocumentPropertiesA function
author: windows-driver-content
description: The AdvancedDocumentProperties function displays a printer-configuration dialog box for the specified printer, allowing the user to configure that printer.
old-location: gdi\advanceddocumentproperties.htm
old-project: printdocs
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AdvancedDocumentProperties, AdvancedDocumentProperties function [Windows GDI], AdvancedDocumentPropertiesA, AdvancedDocumentPropertiesW, _win32_AdvancedDocumentProperties, gdi.advanceddocumentproperties, winspool/AdvancedDocumentProperties, winspool/AdvancedDocumentPropertiesA, winspool/AdvancedDocumentPropertiesW
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
req.unicode-ansi: AdvancedDocumentPropertiesW (Unicode) and AdvancedDocumentPropertiesA (ANSI)
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
-	Winspool.drv
api_name:
-	AdvancedDocumentProperties
-	AdvancedDocumentPropertiesA
-	AdvancedDocumentPropertiesW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AdvancedDocumentPropertiesA function


## -description


The <b>AdvancedDocumentProperties</b> function displays a printer-configuration dialog box for the specified printer, allowing the user to configure that printer.

This function is a special case of the <a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a> function. For more details, see the Remarks section.


## -parameters




### -param hWnd [in]

A handle to the parent window of the printer-configuration dialog box.


### -param hPrinter [in]

A handle to a printer object. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pDeviceName [in]

A pointer to a null-terminated string specifying the name of the device for which a printer-configuration dialog box should be displayed.


### -param pDevModeOutput [out]

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that will contain the configuration data specified by the user.


### -param pDevModeInput [in]

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that contains the configuration data used to initialize the controls of the printer-configuration dialog box.


## -returns



If the <a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a> function with these parameters is successful, the return value of <b>AdvancedDocumentProperties</b> is 1. Otherwise, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
This function can only display the printer-configuration dialog box so a user can configure it. For more control, use <a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a>. The input parameters for this function are passed directly to <b>DocumentProperties</b> and the <i>fMode</i> value is set to DM_IN_BUFFER | DM_IN_PROMPT | DM_OUT_BUFFER. Unlike <b>DocumentProperties</b>, this function only returns 1 or 0. Thus, you cannot determine the required size of <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> by setting <i>pDevMode</i> to zero.

An application can obtain the name pointed to by the <i>pDeviceName</i> parameter by calling the <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a> function and then examining the <b>pPrinterName</b> member of the <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a>



<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a>



<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

