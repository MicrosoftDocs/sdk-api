---
UID: NS:winspool._CORE_PRINTER_DRIVERW
title: "_CORE_PRINTER_DRIVERW"
author: windows-driver-content
description: Represents a printer driver on which other printer drivers depend.
old-location: gdi\core_printer_driver.htm
old-project: printdocs
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCORE_PRINTER_DRIVERW, CORE_PRINTER_DRIVER, CORE_PRINTER_DRIVER structure [Windows GDI], CORE_PRINTER_DRIVERW, PCORE_PRINTER_DRIVER, PCORE_PRINTER_DRIVER structure pointer [Windows GDI], _CORE_PRINTER_DRIVERA, _CORE_PRINTER_DRIVERW, _win32_CORE_PRINTER_DRIVER_str, gdi.core_printer_driver, winspool/CORE_PRINTER_DRIVER, winspool/PCORE_PRINTER_DRIVER, winspool/_CORE_PRINTER_DRIVERA, winspool/_CORE_PRINTER_DRIVERW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_CORE_PRINTER_DRIVERW (Unicode) and _CORE_PRINTER_DRIVERA (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CORE_PRINTER_DRIVERW, *PCORE_PRINTER_DRIVERW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	CORE_PRINTER_DRIVER
-	_CORE_PRINTER_DRIVERA
-	_CORE_PRINTER_DRIVERW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _CORE_PRINTER_DRIVERW structure


## -description



Represents a printer driver on which other printer drivers depend.




## -struct-fields




### -field CoreDriverGUID

The GUID of the core printer driver.


### -field ftDriverDate

The date and time of the latest version of the core printer driver.


### -field dwlDriverVersion

The version ID of the latest version of the core printer driver.


### -field szPackageID

 




#### - szPackageID[MAX_PATH]

The path to the driver package that contains the core printer driver.


## -remarks



This structure can represent a manufacturer's base driver on which the drivers for various printer models are dependent.




## -see-also




<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

