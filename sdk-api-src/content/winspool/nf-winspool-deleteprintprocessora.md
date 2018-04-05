---
UID: NF:winspool.DeletePrintProcessorA
title: DeletePrintProcessorA function
author: windows-driver-content
description: The DeletePrintProcessor function removes a print processor added by the AddPrintProcessor function.
old-location: gdi\deleteprintprocessor.htm
old-project: printdocs
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeletePrintProcessor, DeletePrintProcessor function [Windows GDI], DeletePrintProcessorA, DeletePrintProcessorW, _win32_DeletePrintProcessor, gdi.deleteprintprocessor, winspool/DeletePrintProcessor, winspool/DeletePrintProcessorA, winspool/DeletePrintProcessorW
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
req.unicode-ansi: DeletePrintProcessorW (Unicode) and DeletePrintProcessorA (ANSI)
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
-	DeletePrintProcessor
-	DeletePrintProcessorA
-	DeletePrintProcessorW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePrintProcessorA function


## -description


The <b>DeletePrintProcessor</b> function removes a print processor added by the <a href="https://msdn.microsoft.com/99899cee-f74d-4405-8ea5-616e3769aba9">AddPrintProcessor</a> function.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server from which the processor is to be removed. If this parameter is <b>NULL</b>, the printer processor is removed locally.


### -param pEnvironment [in]

A pointer to a null-terminated string that specifies the environment from which the processor is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64). If this parameter is <b>NULL</b>, the processor is removed from the current environment of the calling application and client machine (not of the destination application and print server). <b>NULL</b> is the recommended value, as it provides maximum portability.


### -param pPrintProcessorName [in]

A pointer to a null-terminated string that specifies the name of the processor to be removed.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The caller must have the <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeLoadDriverPrivilege</a>.




## -see-also




<a href="https://msdn.microsoft.com/99899cee-f74d-4405-8ea5-616e3769aba9">AddPrintProcessor</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

