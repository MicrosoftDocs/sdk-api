---
UID: NS:winspool._DRIVER_INFO_5W
title: "_DRIVER_INFO_5W"
author: windows-driver-content
description: The DRIVER_INFO_5 structure contains printer driver information.
old-location: gdi\driver_info_5.htm
old-project: printdocs
ms.assetid: 6fb63a9f-5227-46a3-97dc-8de1968e9d63
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPDRIVER_INFO_5W, *PDRIVER_INFO_5W, DRIVER_INFO_5, DRIVER_INFO_5 structure [Windows GDI], DRIVER_INFO_5W, PDRIVER_INFO_5, PDRIVER_INFO_5 structure pointer [Windows GDI], _DRIVER_INFO_5A, _DRIVER_INFO_5W, _win32_DRIVER_INFO_5_str, gdi.driver_info_5, winspool/DRIVER_INFO_5, winspool/PDRIVER_INFO_5, winspool/_DRIVER_INFO_5A, winspool/_DRIVER_INFO_5W"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_DRIVER_INFO_5W (Unicode) and _DRIVER_INFO_5A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRIVER_INFO_5W, *PDRIVER_INFO_5W, *LPDRIVER_INFO_5W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	DRIVER_INFO_5
-	_DRIVER_INFO_5A
-	_DRIVER_INFO_5W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DRIVER_INFO_5W structure


## -description



The <b>DRIVER_INFO_5</b> structure contains printer driver information.




## -struct-fields




### -field cVersion

The operating system version for which the driver was written. The supported value is 3.


### -field pName

Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).


### -field pEnvironment

Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).


### -field pDriverPath

Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\DRIVERS\Pscript.dll).


### -field pDataFile

Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\DRIVERS\Qms810.ppd).


### -field pConfigFile

Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\DRIVERS\Pscrptui.dll).


### -field dwDriverAttributes

Driver attributes, like UMPD/KMPD.


### -field dwConfigVersion

Number of times the configuration file for this driver has been upgraded or downgraded since the last spooler restart.


### -field dwDriverVersion

Number of times the driver file for this driver has been upgraded or downgraded since the last spooler restart.


## -see-also




<a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>



<a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a>



<a href="https://msdn.microsoft.com/93f859b4-1005-4359-8029-9536d6eeb7e7">GetPrinterDriver</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

