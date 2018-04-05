---
UID: NF:winspool.AddPrintProcessorW
title: AddPrintProcessorW function
author: windows-driver-content
description: The AddPrintProcessor function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.
old-location: gdi\addprintprocessor.htm
old-project: printdocs
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AddPrintProcessor, AddPrintProcessor function [Windows GDI], AddPrintProcessorA, AddPrintProcessorW, _win32_AddPrintProcessor, gdi.addprintprocessor, winspool/AddPrintProcessor, winspool/AddPrintProcessorA, winspool/AddPrintProcessorW
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
req.unicode-ansi: AddPrintProcessorW (Unicode) and AddPrintProcessorA (ANSI)
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
-	AddPrintProcessor
-	AddPrintProcessorA
-	AddPrintProcessorW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AddPrintProcessorW function


## -description


The <b>AddPrintProcessor</b> function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the print processor should be installed. If this parameter is <b>NULL</b>, the print processor is installed locally.


### -param pEnvironment [in]

A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64). If this parameter is <b>NULL</b>, the current environment of the caller/client (not of the destination/server) is used.


### -param pPathName [in]

A pointer to a null-terminated string that specifies the name of the file that contains the print processor. This file must be in the system print-processor directory.


### -param pPrintProcessorName [in]

A pointer to a null-terminated string that specifies the name of the print processor.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The caller must have the <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeLoadDriverPrivilege</a>.

Before calling the <b>AddPrintProcessor</b> function, an application should verify that the file containing the print processor is stored in the system print-processor directory. An application can retrieve the name of the system print-processor directory by calling the <a href="https://msdn.microsoft.com/a2443cfd-e5ba-41c6-aaf4-45051a3d0e26">GetPrintProcessorDirectory</a> function.

An application can determine the name of existing print processors by calling the <a href="https://msdn.microsoft.com/98c9185c-c89d-4b4e-8c1e-7e22b315f188">EnumPrintProcessors</a> function.




## -see-also




<a href="https://msdn.microsoft.com/98c9185c-c89d-4b4e-8c1e-7e22b315f188">EnumPrintProcessors</a>



<a href="https://msdn.microsoft.com/a2443cfd-e5ba-41c6-aaf4-45051a3d0e26">GetPrintProcessorDirectory</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

