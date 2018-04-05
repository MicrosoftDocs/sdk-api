---
UID: NF:winspool.GetCorePrinterDriversW
title: GetCorePrinterDriversW function
author: windows-driver-content
description: Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.
old-location: gdi\getcoreprinterdrivers.htm
old-project: printdocs
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetCorePrinterDrivers, GetCorePrinterDrivers function [Windows GDI], GetCorePrinterDriversA, GetCorePrinterDriversW, _win32_GetCorePrinterDrivers, gdi.getcoreprinterdrivers, winspool/GetCorePrinterDrivers, winspool/GetCorePrinterDriversA, winspool/GetCorePrinterDriversW
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
req.unicode-ansi: GetCorePrinterDriversW (Unicode) and GetCorePrinterDriversA (ANSI)
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
-	GetCorePrinterDrivers
-	GetCorePrinterDriversA
-	GetCorePrinterDriversW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetCorePrinterDriversW function


## -description


Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.


## -parameters




### -param pszServer [in]

A pointer to a constant, null-terminated string that specifies the name of the print server. Use <b>NULL</b> for the local computer.


### -param pszEnvironment [in]

A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86). This can be <b>NULL</b>.


### -param pszzCoreDriverDependencies [in]

A pointer to a null-terminated multi-string that specifies the GUIDs of the core printer drivers.


### -param cCorePrinterDrivers [in]

The number of strings in <i>pszzCoreDriverDependencies</i>.


### -param pCorePrinterDrivers [out]

A pointer to an array of one or more <a href="https://msdn.microsoft.com/b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38">CORE_PRINTER_DRIVER</a> structures.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> will contain an error code.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.




## -remarks



This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.




## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

