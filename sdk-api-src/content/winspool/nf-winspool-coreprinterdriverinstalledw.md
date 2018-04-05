---
UID: NF:winspool.CorePrinterDriverInstalledW
title: CorePrinterDriverInstalledW function
author: windows-driver-content
description: The CorePrinterDriverInstalled function reports whether a core printer driver with a specified GUID, date, and version is installed.
old-location: gdi\coreprinterdriverinstalled.htm
old-project: printdocs
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CorePrinterDriverInstalled, CorePrinterDriverInstalled function [Windows GDI], CorePrinterDriverInstalledA, CorePrinterDriverInstalledW, _win32_CorePrinterDriverInstalled, gdi.coreprinterdriverinstalled, winspool/CorePrinterDriverInstalled, winspool/CorePrinterDriverInstalledA, winspool/CorePrinterDriverInstalledW
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
req.unicode-ansi: CorePrinterDriverInstalledW (Unicode) and CorePrinterDriverInstalledA (ANSI)
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
-	CorePrinterDriverInstalled
-	CorePrinterDriverInstalledA
-	CorePrinterDriverInstalledW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CorePrinterDriverInstalledW function


## -description


The <b>CorePrinterDriverInstalled</b> function reports whether a core printer driver with a specified GUID, date, and version is installed.


## -parameters




### -param pszServer [in]

Pointer to a constant, null-terminated string that specifies the name of the print server. Use <b>NULL</b> for the local computer.


### -param pszEnvironment [in]

Pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86). This can be <b>NULL</b>.


### -param CoreDriverGUID [in]

The GUID of the core printer driver.


### -param ftDriverDate [in]

The date of the core printer driver.


### -param dwlDriverVersion [in]

The version of the core printer driver.


### -param pbDriverInstalled [out]

A pointer to <b>TRUE</b> if the driver, or a newer version, is installed, <b>FALSE</b> otherwise.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> will contain an error code.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

