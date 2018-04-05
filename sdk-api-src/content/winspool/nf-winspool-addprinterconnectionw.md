---
UID: NF:winspool.AddPrinterConnectionW
title: AddPrinterConnectionW function
author: windows-driver-content
description: The AddPrinterConnection function adds a connection to the specified printer for the current user.
old-location: gdi\addprinterconnection.htm
old-project: printdocs
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AddPrinterConnection, AddPrinterConnection function [Windows GDI], AddPrinterConnectionA, AddPrinterConnectionW, _win32_AddPrinterConnection, gdi.addprinterconnection, winspool/AddPrinterConnection, winspool/AddPrinterConnectionA, winspool/AddPrinterConnectionW
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
req.unicode-ansi: AddPrinterConnectionW (Unicode) and AddPrinterConnectionA (ANSI)
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
-	AddPrinterConnection
-	AddPrinterConnectionA
-	AddPrinterConnectionW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AddPrinterConnectionW function


## -description


The <b>AddPrinterConnection</b> function adds a connection to the specified printer for the current user.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of a printer to which the current user wishes to establish a connection.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
When Windows makes a connection to a printer, it may need to copy printer driver files to the server to which the printer is attached. If the user does not have permission to copy files to the appropriate location, the <b>AddPrinterConnection</b> function fails, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_ACCESS_DENIED.

A printer connection established by calling <b>AddPrinterConnection</b> will be enumerated when <a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a> is called with <i>dwType</i> set to PRINTER_ENUM_CONNECTION.




## -see-also




<a href="https://msdn.microsoft.com/7cb9108b-8b65-4af3-88c8-a69771ed8e3f">ConnectToPrinterDlg</a>



<a href="https://msdn.microsoft.com/7b056eea-fbd9-4a08-a2dc-7326caeec387">DeletePrinterConnection</a>



<a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

