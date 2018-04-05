---
UID: NF:winspool.GetPrinterDriverDirectoryW
title: GetPrinterDriverDirectoryW function
author: windows-driver-content
description: The GetPrinterDriverDirectory function retrieves the path of the printer-driver directory.
old-location: gdi\getprinterdriverdirectory.htm
old-project: printdocs
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetPrinterDriverDirectory, GetPrinterDriverDirectory function [Windows GDI], GetPrinterDriverDirectoryA, GetPrinterDriverDirectoryW, _win32_GetPrinterDriverDirectory, gdi.getprinterdriverdirectory, winspool/GetPrinterDriverDirectory, winspool/GetPrinterDriverDirectoryA, winspool/GetPrinterDriverDirectoryW
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
req.unicode-ansi: GetPrinterDriverDirectoryW (Unicode) and GetPrinterDriverDirectoryA (ANSI)
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
-	Ext-MS-Win-printer-Winspool-l1-1-1.dll
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	GetPrinterDriverDirectory
-	GetPrinterDriverDirectoryA
-	GetPrinterDriverDirectoryW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPrinterDriverDirectoryW function


## -description


The <b>GetPrinterDriverDirectory</b> function retrieves the path of the printer-driver directory.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the printer driver resides. If this parameter is <b>NULL</b>, the local driver-directory path is retrieved.


### -param pEnvironment [in]

A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64). If this parameter is <b>NULL</b>, the current environment of the calling application and client machine (not of the destination application and print server) is used.


### -param Level [in]

The structure level. This value must be 1.


### -param pDriverDirectory [out]

A pointer to a buffer that receives the path.


### -param cbBuf [in]

The size of the buffer to which <i>pDriverDirectory</i> points.


### -param pcbNeeded [out]

A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if <i>cbBuf</i> is too small.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

