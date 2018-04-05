---
UID: NF:winspool.DeletePrinterConnectionW
title: DeletePrinterConnectionW function
author: windows-driver-content
description: The DeletePrinterConnection function deletes a connection to a printer that was established by a call to AddPrinterConnection or ConnectToPrinterDlg.
old-location: gdi\deleteprinterconnection.htm
old-project: printdocs
ms.assetid: 7b056eea-fbd9-4a08-a2dc-7326caeec387
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeletePrinterConnection, DeletePrinterConnection function [Windows GDI], DeletePrinterConnectionA, DeletePrinterConnectionW, _win32_DeletePrinterConnection, gdi.deleteprinterconnection, winspool/DeletePrinterConnection, winspool/DeletePrinterConnectionA, winspool/DeletePrinterConnectionW
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
req.unicode-ansi: DeletePrinterConnectionW (Unicode) and DeletePrinterConnectionA (ANSI)
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
-	DeletePrinterConnection
-	DeletePrinterConnectionA
-	DeletePrinterConnectionW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePrinterConnectionW function


## -description


The <b>DeletePrinterConnection</b> function deletes a connection to a printer that was established by a call to <a href="https://msdn.microsoft.com/6decf89a-1411-4e7e-aa20-60e7068658c2">AddPrinterConnection</a> or <a href="https://msdn.microsoft.com/7cb9108b-8b65-4af3-88c8-a69771ed8e3f">ConnectToPrinterDlg</a>.


## -parameters




### -param pName [in]

Pointer to a null-terminated string that specifies the name of the printer connection to delete.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <b>DeletePrinterConnection</b> function does not delete any printer driver files that were copied to the server to which the printer is attached.




## -see-also




<a href="https://msdn.microsoft.com/6decf89a-1411-4e7e-aa20-60e7068658c2">AddPrinterConnection</a>



<a href="https://msdn.microsoft.com/5ae98157-5978-449e-beb1-4787110925fa">AddPrinterConnection2</a>



<a href="https://msdn.microsoft.com/7cb9108b-8b65-4af3-88c8-a69771ed8e3f">ConnectToPrinterDlg</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

