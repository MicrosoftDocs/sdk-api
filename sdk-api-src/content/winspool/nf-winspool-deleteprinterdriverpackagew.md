---
UID: NF:winspool.DeletePrinterDriverPackageW
title: DeletePrinterDriverPackageW function
author: windows-driver-content
description: Deletes a printer driver package from the driver store.
old-location: gdi\deleteprinterdriverpackage.htm
old-project: printdocs
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeletePrinterDriverPackage, DeletePrinterDriverPackage function [Windows GDI], DeletePrinterDriverPackageA, DeletePrinterDriverPackageW, _win32_DeletePrinterDriverPackage, gdi.deleteprinterdriverpackage, winspool/DeletePrinterDriverPackage, winspool/DeletePrinterDriverPackageA, winspool/DeletePrinterDriverPackageW
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
req.unicode-ansi: DeletePrinterDriverPackageW (Unicode) and DeletePrinterDriverPackageA (ANSI)
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
-	DeletePrinterDriverPackage
-	DeletePrinterDriverPackageA
-	DeletePrinterDriverPackageW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePrinterDriverPackageW function


## -description


Deletes a printer driver package from the driver store.


## -parameters




### -param pszServer [in]

A pointer to a constant, null-terminated string that specifies the name of the print server from which the driver package is being deleted. A <b>NULL</b> pointer value means the local computer.


### -param pszInfPath [in]

A pointer to a constant, null-terminated string that specifies the path to the driver's *.inf file.


### -param pszEnvironment [in]

A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86). This can be <b>NULL</b>.


## -returns



S_OK, if the operation succeeds.

E_ACCESSDENIED, if the package was shipped with Windows.

HRESULT_CODE(ERROR_PRINT_DRIVER_PACKAGE_IN_USE), if the package is being used.

Otherwise the <b>HRESULT</b> will contain an error code.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The driver store is typically %windir%\inf or %windir%\System32\DriverStore\FileRepository.

A driver package that shipped with Windows cannot be removed with this function.

The user must have printer administration privileges.




## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

