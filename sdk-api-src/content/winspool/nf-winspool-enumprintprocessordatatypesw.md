---
UID: NF:winspool.EnumPrintProcessorDatatypesW
title: EnumPrintProcessorDatatypesW function
author: windows-driver-content
description: The EnumPrintProcessorDatatypes function enumerates the data types that a specified print processor supports.
old-location: gdi\enumprintprocessordatatypes.htm
old-project: printdocs
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EnumPrintProcessorDatatypes, EnumPrintProcessorDatatypes function [Windows GDI], EnumPrintProcessorDatatypesA, EnumPrintProcessorDatatypesW, _win32_EnumPrintProcessorDatatypes, gdi.enumprintprocessordatatypes, winspool/EnumPrintProcessorDatatypes, winspool/EnumPrintProcessorDatatypesA, winspool/EnumPrintProcessorDatatypesW
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
req.unicode-ansi: EnumPrintProcessorDatatypesW (Unicode) and EnumPrintProcessorDatatypesA (ANSI)
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
-	EnumPrintProcessorDatatypes
-	EnumPrintProcessorDatatypesA
-	EnumPrintProcessorDatatypesW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumPrintProcessorDatatypesW function


## -description


The <b>EnumPrintProcessorDatatypes</b> function enumerates the data types that a specified print processor supports.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the print processor resides. If this parameter is <b>NULL</b>, the data types for the local print processor are enumerated.


### -param pPrintProcessorName [in]

A pointer to a null-terminated string that specifies the name of the print processor whose data types are enumerated.


### -param Level [in]

The type of information returned in the <i>pDatatypes</i> buffer. This parameter must be 1.


### -param pDatatypes [out]

A pointer to a buffer that receives an array of <a href="https://msdn.microsoft.com/6169006c-12d4-4608-865c-732f04107f9f">DATATYPES_INFO_1</a> structures. Each structure describes an available data type. The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.

To determine the required buffer size, call <b>EnumPrintProcessorDatatypes</b> with <i>cbBuf</i> set to zero. <b>EnumPrintProcessorDatatypes</b> fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, and the <i>pcbNeeded</i> parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.


### -param cbBuf [in]

The size, in bytes, of the buffer pointed to by <i>pDatatypes</i>.


### -param pcbNeeded [out]

A pointer to a variable that receives the number of bytes copied to the <i>pDatatypes</i> buffer if the function succeeds. If the buffer is too small, the function fails and the variable receives the number of bytes required.


### -param pcReturned [out]

A pointer to a variable that receives the number of structures returned in the <i>pDatatypes</i> buffer. This is the number of supported data types.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
v

Starting with Windows Vista, the data type information from remote print servers  is retrieved from a local cache.




## -see-also




<a href="https://msdn.microsoft.com/6169006c-12d4-4608-865c-732f04107f9f">DATATYPES_INFO_1</a>



<a href="https://msdn.microsoft.com/98c9185c-c89d-4b4e-8c1e-7e22b315f188">EnumPrintProcessors</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

