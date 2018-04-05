---
UID: NF:winspool.AddPrinterConnection2W
title: AddPrinterConnection2W function
author: windows-driver-content
description: Adds a connection to the specified printer for the current user and specifies connection details.
old-location: gdi\addprinterconnection2.htm
old-project: printdocs
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AddPrinterConnection2, AddPrinterConnection2 function [Windows GDI], AddPrinterConnection2W, _win32_AddPrinterConnection2, gdi.addprinterconnection2, winspool/AddPrinterConnection2, winspool/AddPrinterConnection2W
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddPrinterConnection2W (Unicode)
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
-	AddPrinterConnection2
-	AddPrinterConnection2W
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AddPrinterConnection2W function


## -description


Adds a connection to the specified printer for the current user and specifies connection details.


## -parameters




### -param hWnd [in]

A handle to the parent window in which the dialog box will be displayed if the print system must download a printer driver from the print server for this connection.


### -param pszName [in]

A pointer to a constant null-terminated string specifying the name of the printer to which the current user wishes to connect.


### -param dwLevel

The version of the structure pointed to by <i>pConnectionInfo</i>. Currently, only level 1 is defined so the value of <i>dwLevel</i> must be 1.


### -param pConnectionInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/afac3f91-74eb-46f7-94b4-d37b2b8a32a4">PRINTER_CONNECTION_INFO_1</a> structure. See the Remarks section for more about this parameter.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
When Windows Vista makes a connection to a printer, it may need to copy printer driver files from the server to which the printer is attached. If the user does not have permission to copy files to the appropriate location, the <b>AddPrinterConnection2</b> function fails and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_ACCESS_DENIED.

If the printer driver files must be copied from the print server but cannot be copied silently due to the group policies that are in effect and PRINTER_CONNECTION_NO_UI is set in <i>pConnectionInfo-&gt;dwFlags</i>, no dialog boxes will be displayed and the call will fail.

If the local printer driver can be used to render print jobs for this printer and the version of the local driver must not match the version of the printer driver on the server, set PRINTER_CONNECTION_MISMATCH in <i>pConnectionInfo-&gt;dwFlags</i> and assign the pointer to a string variable that contains the path to the local printer driver to <i>pConnectionInfo-&gt;pszDriverName</i>.

A printer connection that is established by calling <b>AddPrinterConnection2</b> will be enumerated when <a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a> is called with <i>dwType</i> set to PRINTER_ENUM_CONNECTION.

The ANSI version of this function, <b>AddPrinterConnection2A</b>, is not supported and returns <b>ERROR_NOT_SUPPORTED</b>.




## -see-also




<a href="https://msdn.microsoft.com/7cb9108b-8b65-4af3-88c8-a69771ed8e3f">ConnectToPrinterDlg</a>



<a href="https://msdn.microsoft.com/7b056eea-fbd9-4a08-a2dc-7326caeec387">DeletePrinterConnection</a>



<a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

