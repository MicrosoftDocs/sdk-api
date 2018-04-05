---
UID: NF:winspool.GetPrintProcessorDirectoryA
title: GetPrintProcessorDirectoryA function
author: windows-driver-content
description: The GetPrintProcessorDirectory function retrieves the path to the print processor directory on the specified server.
old-location: gdi\getprintprocessordirectory.htm
old-project: printdocs
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetPrintProcessorDirectory, GetPrintProcessorDirectory function [Windows GDI], GetPrintProcessorDirectoryA, GetPrintProcessorDirectoryW, _win32_GetPrintProcessorDirectory, gdi.getprintprocessordirectory, winspool/GetPrintProcessorDirectory, winspool/GetPrintProcessorDirectoryA, winspool/GetPrintProcessorDirectoryW
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
req.unicode-ansi: GetPrintProcessorDirectoryW (Unicode) and GetPrintProcessorDirectoryA (ANSI)
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
-	GetPrintProcessorDirectory
-	GetPrintProcessorDirectoryA
-	GetPrintProcessorDirectoryW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPrintProcessorDirectoryA function


## -description


The <b>GetPrintProcessorDirectory</b> function retrieves the path to the print processor directory on the specified server.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server. If this parameter is <b>NULL</b>, a local path is returned.


### -param pEnvironment [in]

A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64). If this parameter is <b>NULL</b>, the current environment of the calling application and client machine (not of the destination application and print server) is used.


### -param Level [in]

The structure level. This value must be 1.


### -param pPrintProcessorInfo [out]

A pointer to a buffer that receives the path. Note that, for operating systems prior to Windows Server 2003 SP 1, the path is in the local format for the server, not the true remote format. For example, the path is given as "%Windir%\System32\Spool\Prtprocs\%Environment%" instead of "\\ServerName\Print$\Prtprocs\%Environment%", even when called for a remote server. For the operating systems Windows Server 2003 SP 1 and later, the true remote path is returned.


### -param cbBuf [in]

The size of the buffer pointed to by <i>pPrintProcessorInfo</i>.


### -param pcbNeeded [out]

A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if <i>cbBuf</i> is too small.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/99899cee-f74d-4405-8ea5-616e3769aba9">AddPrintProcessor</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

