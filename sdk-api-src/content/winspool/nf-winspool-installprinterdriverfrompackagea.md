---
UID: NF:winspool.InstallPrinterDriverFromPackageA
title: InstallPrinterDriverFromPackageA function
author: windows-driver-content
description: Installs a printer driver from a driver package that is in the print server's driver store.
old-location: gdi\installprinterdriverfrompackage.htm
old-project: printdocs
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: InstallPrinterDriverFromPackage, InstallPrinterDriverFromPackage function [Windows GDI], InstallPrinterDriverFromPackageA, InstallPrinterDriverFromPackageW, _win32_InstallPrinterDriverFromPackage, gdi.installprinterdriverfrompackage, winspool/InstallPrinterDriverFromPackage, winspool/InstallPrinterDriverFromPackageA, winspool/InstallPrinterDriverFromPackageW
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
req.unicode-ansi: InstallPrinterDriverFromPackageW (Unicode) and InstallPrinterDriverFromPackageA (ANSI)
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
-	InstallPrinterDriverFromPackage
-	InstallPrinterDriverFromPackageA
-	InstallPrinterDriverFromPackageW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# InstallPrinterDriverFromPackageA function


## -description


Installs a printer driver from a driver package that is in the print server's driver store.


## -parameters




### -param pszServer [in]

A pointer to a constant, null-terminated string that specifies the name of the print server. <b>NULL</b> means the local computer.


### -param pszInfPath [in]

A pointer to a constant, null-terminated string that specifies the driver store path to the print driver's .inf file. <b>NULL</b> means the driver is in an inf file that shipped with Windows.


### -param pszDriverName [in]

A pointer to a constant, null-terminated string that specifies the name of the driver.


### -param pszEnvironment [in]

A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86). This can be <b>NULL</b>.


### -param dwFlags [in]

This can only be 0 or IPDFP_COPY_ALL_FILES. A value of 0 means that the printer driver must be added and any files in the printer driver directory that are newer than corresponding files currently in use must be copied. A value of IPDFP_COPY_ALL_FILES means the printer driver and all the files in the printer driver directory must be added. The file time stamps are ignored when <i>dwFlags</i> has a value of IPDFP_COPY_ALL_FILES.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> will contain an error code.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The driver store is typically either %windir%\inf or %windir%\System32\DriverStore\FileRepository.

<b>InstallPrinterDriverFromPackage</b> also installs other files in the package, such as color profiles and print processors.

Users must have printer administration rights to install either on a remote computer or on the local computer when the user is logged in with Terminal Services.

Only signed packages can be installed on a remote computer.




## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

