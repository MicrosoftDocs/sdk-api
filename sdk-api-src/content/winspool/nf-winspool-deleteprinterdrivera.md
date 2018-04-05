---
UID: NF:winspool.DeletePrinterDriverA
title: DeletePrinterDriverA function
author: windows-driver-content
description: The DeletePrinterDriver function removes the specified printer-driver name from the list of names of supported drivers on a server.
old-location: gdi\deleteprinterdriver.htm
old-project: printdocs
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeletePrinterDriver, DeletePrinterDriver function [Windows GDI], DeletePrinterDriverA, DeletePrinterDriverW, _win32_DeletePrinterDriver, gdi.deleteprinterdriver, winspool/DeletePrinterDriver, winspool/DeletePrinterDriverA, winspool/DeletePrinterDriverW
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
req.unicode-ansi: DeletePrinterDriverW (Unicode) and DeletePrinterDriverA (ANSI)
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
-	DeletePrinterDriver
-	DeletePrinterDriverA
-	DeletePrinterDriverW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePrinterDriverA function


## -description


The <b>DeletePrinterDriver</b> function removes the specified printer-driver name from the list of names of supported drivers on a server.

To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the <a href="https://msdn.microsoft.com/1a3d7c7f-1d45-4877-a8f7-a77f40e3c319">DeletePrinterDriverEx</a> function.

<b>DeletePrinterDriver</b> deletes a driver only if no version of the driver is in use for the specified environment. <a href="https://msdn.microsoft.com/1a3d7c7f-1d45-4877-a8f7-a77f40e3c319">DeletePrinterDriverEx</a> can delete specific versions of the driver.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted. If this parameter is <b>NULL</b>, the printer-driver name will be removed locally.


### -param pEnvironment [in]

A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows x86, Windows IA64, or Windows x64). If this parameter is <b>NULL</b>, the driver name is deleted from the current environment of the calling application and client machine (not of the destination application and print server).


### -param pDriverName [in]

A pointer to a null-terminated string specifying the name of the driver that should be deleted.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The caller must have the <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeLoadDriverPrivilege</a>.

The <b>DeletePrinterDriver</b> function does not delete the associated files, it merely removes the driver name from the list returned by the <a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a> function.

Before calling <b>DeletePrinterDriver</b>, you must delete all printer objects that use the printer driver.




## -see-also




<a href="https://msdn.microsoft.com/1a3d7c7f-1d45-4877-a8f7-a77f40e3c319">DeletePrinterDriverEx</a>



<a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

