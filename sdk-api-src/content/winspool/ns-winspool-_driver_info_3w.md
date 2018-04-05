---
UID: NS:winspool._DRIVER_INFO_3W
title: "_DRIVER_INFO_3W"
author: windows-driver-content
description: The DRIVER_INFO_3 structure contains printer driver information.
old-location: gdi\driver_info_3.htm
old-project: printdocs
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPDRIVER_INFO_3W, *PDRIVER_INFO_3W, DRIVER_INFO_3, DRIVER_INFO_3 structure [Windows GDI], DRIVER_INFO_3W, PDRIVER_INFO_3, PDRIVER_INFO_3 structure pointer [Windows GDI], _DRIVER_INFO_3A, _DRIVER_INFO_3W, _win32_DRIVER_INFO_3_str, gdi.driver_info_3, winspool/DRIVER_INFO_3, winspool/PDRIVER_INFO_3, winspool/_DRIVER_INFO_3A, winspool/_DRIVER_INFO_3W"
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
req.unicode-ansi: "_DRIVER_INFO_3W (Unicode) and _DRIVER_INFO_3A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRIVER_INFO_3W, *PDRIVER_INFO_3W, *LPDRIVER_INFO_3W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	DRIVER_INFO_3
-	_DRIVER_INFO_3A
-	_DRIVER_INFO_3W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DRIVER_INFO_3W structure


## -description



The <b>DRIVER_INFO_3</b> structure contains printer driver information.




## -struct-fields




### -field cVersion

The operating system version for which the driver was written. The supported values are 3 and 4, which represent the V3 and V4 drivers, respectively.


### -field pName

A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").


### -field pEnvironment

A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).


### -field pDriverPath

A pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "C:\DRIVERS\Pscript.dll").


### -field pDataFile

A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "C:\DRIVERS\Qms810.ppd").


### -field pConfigFile

A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, "C:\DRIVERS\Pscrptui.dll").


### -field pHelpFile

A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.


### -field pDependentFiles

A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings. Each null-terminated string in the buffer contains the name of a file the driver depends on. The sequence of strings is terminated by an empty, zero-length string. If <b>pDependentFiles</b> is not <b>NULL</b> and does not contain any file names, it will point to a buffer that contains two empty strings.


### -field pMonitorName

A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor"). This member can be <b>NULL</b> and should be specified only for printers capable of bidirectional communication.


### -field pDefaultDataType

A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").


## -see-also




<a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>



<a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a>



<a href="https://msdn.microsoft.com/93f859b4-1005-4359-8029-9536d6eeb7e7">GetPrinterDriver</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

