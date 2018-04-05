---
UID: NF:winspool.DeletePrinterDataA
title: DeletePrinterDataA function
author: windows-driver-content
description: The DeletePrinterData function deletes specified configuration data for a printer. A printer's configuration data consists of a set of named and typed values. The DeletePrinterData function deletes one of these values, specified by its value name.
old-location: gdi\deleteprinterdata.htm
old-project: printdocs
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeletePrinterData, DeletePrinterData function [Windows GDI], DeletePrinterDataA, DeletePrinterDataW, _win32_DeletePrinterData, gdi.deleteprinterdata, winspool/DeletePrinterData, winspool/DeletePrinterDataA, winspool/DeletePrinterDataW
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
req.unicode-ansi: DeletePrinterDataW (Unicode) and DeletePrinterDataA (ANSI)
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
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	DeletePrinterData
-	DeletePrinterDataA
-	DeletePrinterDataW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePrinterDataA function


## -description


The <b>DeletePrinterData</b> function deletes specified configuration data for a printer. A printer's configuration data consists of a set of named and typed values. The <b>DeletePrinterData</b> function deletes one of these values, specified by its value name.

Calling <b>DeletePrinterData</b> is equivalent to calling the <a href="https://msdn.microsoft.com/bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55">DeletePrinterDataEx</a> function with the <i>pKeyName</i>  parameter set to "PrinterDriverData".


## -parameters




### -param hPrinter [in]

A handle to the printer whose configuration data is to be deleted. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pValueName [in]

A pointer to the null-terminated name of the configuration data value to be deleted.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a system error code.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0a4c8436-46fe-4e21-8d55-c5031a3d1b38">EnumPrinterData</a>



<a href="https://msdn.microsoft.com/b5a44b27-a4aa-4e58-9a64-05be87d12ab5">GetPrinterData</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>



<a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a>
 

 

