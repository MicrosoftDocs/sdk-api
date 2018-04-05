---
UID: NF:winspool.EnumPrintProcessorsW
title: EnumPrintProcessorsW function
author: windows-driver-content
description: The EnumPrintProcessors function enumerates the print processors installed on the specified server.
old-location: gdi\enumprintprocessors.htm
old-project: printdocs
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EnumPrintProcessors, EnumPrintProcessors function [Windows GDI], EnumPrintProcessorsA, EnumPrintProcessorsW, _win32_EnumPrintProcessors, gdi.enumprintprocessors, winspool/EnumPrintProcessors, winspool/EnumPrintProcessorsA, winspool/EnumPrintProcessorsW
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
req.unicode-ansi: EnumPrintProcessorsW (Unicode) and EnumPrintProcessorsA (ANSI)
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
-	EnumPrintProcessors
-	EnumPrintProcessorsA
-	EnumPrintProcessorsW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumPrintProcessorsW function


## -description


The <b>EnumPrintProcessors</b> function enumerates the print processors installed on the specified server.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the print processors reside. If this parameter is <b>NULL</b>, the local print processors are enumerated.


### -param pEnvironment [in]

A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64). If this parameter is <b>NULL</b>, the current environment of the calling application and client machine (not of the destination application and print server) is used.


### -param Level [in]

The type of information returned in the <i>pPrintProcessorInfo</i> buffer. This parameter must be 1.


### -param pPrintProcessorInfo [out]

A pointer to a buffer that receives an array of <a href="https://msdn.microsoft.com/49b272c8-156b-4996-b3fd-92cde831f4ae">PRINTPROCESSOR_INFO_1</a> structures. Each structure describes an available print processor. The buffer must be large enough to receive the array of structures and any strings to which the structure members point.

To determine the required buffer size, call <b>EnumPrintProcessors</b> with <i>cbBuf</i> set to zero. <b>EnumPrintProcessors</b> fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, and the <i>pcbNeeded</i> parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.


### -param cbBuf [in]

The size, in bytes, of the buffer pointed to by <i>pPrintProcessorInfo</i>.


### -param pcbNeeded [out]

A pointer to a variable that receives the number of bytes copied to the <i>pPrintProcessorInfo</i> buffer if the function succeeds. If the buffer is too small, the function fails and the variable receives the number of bytes required.


### -param pcReturned [out]

A pointer to a variable that receives the number of structures returned in the <i>pPrintProcessorInfo</i> buffer.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/99899cee-f74d-4405-8ea5-616e3769aba9">AddPrintProcessor</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548757">EnumPrintProcessorDatatypes</a>



<a href="https://msdn.microsoft.com/49b272c8-156b-4996-b3fd-92cde831f4ae">PRINTPROCESSOR_INFO_1</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

