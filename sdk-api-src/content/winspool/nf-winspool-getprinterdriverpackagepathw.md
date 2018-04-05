---
UID: NF:winspool.GetPrinterDriverPackagePathW
title: GetPrinterDriverPackagePathW function
author: windows-driver-content
description: Retrieves the path to the specified printer driver package on a print server.
old-location: gdi\getprinterdriverpackagepath.htm
old-project: printdocs
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetPrinterDriverPackagePath, GetPrinterDriverPackagePath function [Windows GDI], GetPrinterDriverPackagePathA, GetPrinterDriverPackagePathW, _win32_GetPrinterDriverPackagePath, gdi.getprinterdriverpackagepath, winspool/GetPrinterDriverPackagePath, winspool/GetPrinterDriverPackagePathA, winspool/GetPrinterDriverPackagePathW
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
req.unicode-ansi: GetPrinterDriverPackagePathW (Unicode) and GetPrinterDriverPackagePathA (ANSI)
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
-	Spoolss.dll
api_name:
-	GetPrinterDriverPackagePath
-	GetPrinterDriverPackagePathA
-	GetPrinterDriverPackagePathW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPrinterDriverPackagePathW function


## -description


Retrieves the path to the specified printer driver package on a print server.


## -parameters




### -param pszServer [in]

A pointer to a constant, null-terminated string that specifies the name of the print server. Use <b>NULL</b> for the local computer.


### -param pszEnvironment [in]

A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86). This can be <b>NULL</b>.


### -param pszLanguage [in]

A pointer to a constant, null-terminated string that specifies the <a href="https://msdn.microsoft.com/4d8b769d-0830-4e4e-b284-ce0b21dfe5d4">Multilingual User Interface</a> language for the driver being installed. This can be <b>NULL</b>.


### -param pszPackageID [in]

A pointer to a constant, null-terminated string that specifies the ID of the driver package.


### -param pszDriverPackageCab [in, out]

A pointer to a null-terminated string that specifies the path to the cabinet file for the driver package. This can be <b>NULL</b>. See Remarks.


### -param cchDriverPackageCab [in]

The size, in characters, of the <i>pszDriverPackageCab</i> buffer. This can be <b>NULL</b>.


### -param pcchRequiredSize [out]

A pointer to the required size of the <i>pszDriverPackageCab</i> buffer.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> will contain an error code.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
To obtain a value for <i>cchDriverPackageCab</i>, call the function with <b>NULL</b> as the value of <i>pszDriverPackageCab</i>. Use the value returned in <i>pcchRequiredSize</i> as the value of <i>cchDriverPackageCab</i> and call the function again.

The <i>pszPackageID</i> is typically obtained from a call to <a href="https://msdn.microsoft.com/98acad48-cd42-4d2b-be58-81c1366f6912">GetCorePrinterDrivers</a>.




## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

