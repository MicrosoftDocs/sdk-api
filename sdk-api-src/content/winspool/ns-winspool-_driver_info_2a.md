---
UID: NS:winspool._DRIVER_INFO_2A
title: "_DRIVER_INFO_2A"
author: windows-driver-content
description: The DRIVER_INFO_2 structure identifies a printer driver, the driver version number, the environment for which the driver was written, the name of the file in which the driver is stored, and so on.
old-location: gdi\driver_info_2.htm
old-project: printdocs
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPDRIVER_INFO_2A, *PDRIVER_INFO_2A, DRIVER_INFO_2, DRIVER_INFO_2 structure [Windows GDI], DRIVER_INFO_2A, PDRIVER_INFO_2, PDRIVER_INFO_2 structure pointer [Windows GDI], _DRIVER_INFO_2A, _DRIVER_INFO_2W, _win32_DRIVER_INFO_2_str, gdi.driver_info_2, winspool/DRIVER_INFO_2, winspool/PDRIVER_INFO_2, winspool/_DRIVER_INFO_2A, winspool/_DRIVER_INFO_2W"
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
req.unicode-ansi: "_DRIVER_INFO_2W (Unicode) and _DRIVER_INFO_2A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRIVER_INFO_2A, *PDRIVER_INFO_2A, *LPDRIVER_INFO_2A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	DRIVER_INFO_2
-	_DRIVER_INFO_2A
-	_DRIVER_INFO_2W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DRIVER_INFO_2A structure


## -description



The <b>DRIVER_INFO_2</b> structure identifies a printer driver, the driver version number, the environment for which the driver was written, the name of the file in which the driver is stored, and so on.




## -struct-fields




### -field cVersion

The operating system version for which the driver was written. The supported value is 3.


### -field pName

A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").


### -field pEnvironment

A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).


### -field pDriverPath

A pointer to null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "c:\drivers\pscript.dll").


### -field pDataFile

A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "c:\drivers\Qms810.ppd").


### -field pConfigFile

A pointer to a null-terminated string that specifies a file name or a full path and file name for the device-driver's configuration .dll (for example, "c:\drivers\Pscrptui.dll").


## -see-also




<a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>



<a href="https://msdn.microsoft.com/93f859b4-1005-4359-8029-9536d6eeb7e7">GetPrinterDriver</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

