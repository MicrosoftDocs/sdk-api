---
UID: NS:winspool._DRIVER_INFO_6A
title: "_DRIVER_INFO_6A"
author: windows-driver-content
description: The DRIVER_INFO_6 structure contains printer driver information.
old-location: gdi\driver_info_6.htm
old-project: printdocs
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPDRIVER_INFO_6A, *PDRIVER_INFO_6A, DRIVER_INFO_6, DRIVER_INFO_6 structure [Windows GDI], DRIVER_INFO_6A, LPDRIVER_INFO_6, LPDRIVER_INFO_6 structure pointer [Windows GDI], PDRIVER_INFO_6, PDRIVER_INFO_6 structure pointer [Windows GDI], _DRIVER_INFO_6A, _DRIVER_INFO_6W, _win32_DRIVER_INFO_6_str, gdi.driver_info_6, winspool/DRIVER_INFO_6, winspool/LPDRIVER_INFO_6, winspool/PDRIVER_INFO_6, winspool/_DRIVER_INFO_6A, winspool/_DRIVER_INFO_6W"
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
req.unicode-ansi: "_DRIVER_INFO_6W (Unicode) and _DRIVER_INFO_6A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRIVER_INFO_6A, *PDRIVER_INFO_6A, *LPDRIVER_INFO_6A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	DRIVER_INFO_6
-	_DRIVER_INFO_6A
-	_DRIVER_INFO_6W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DRIVER_INFO_6A structure


## -description



The <b>DRIVER_INFO_6</b> structure contains printer driver information.




## -struct-fields




### -field cVersion

The operating system version for which the driver was written. The supported value is 3.


### -field pName

Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).


### -field pEnvironment

Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows NT x86, Windows IA64, and Windows x64.


### -field pDriverPath

Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\DRIVERS\Pscript.dll).


### -field pDataFile

Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\DRIVERS\Qms810.ppd).


### -field pConfigFile

Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\DRIVERS\Pscrptui.dll).


### -field pHelpFile

Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\DRIVERS\Pscrptui.hlp).


### -field pDependentFiles

A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings. Each null-terminated string in the buffer contains the name of a file the driver depends on. The sequence of strings is terminated by an empty, zero-length string. If <b>pDependentFiles</b> is not <b>NULL</b> and does not contain any file names, it will point to a buffer that contains two empty strings.


### -field pMonitorName

A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor"). This member can be <b>NULL</b> and should be specified only for printers capable of bidirectional communication.


### -field pDefaultDataType

A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").


### -field pszzPreviousNames

A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver. For example, OldName1\0OldName2\0\0.


### -field ftDriverDate

The date of the driver package, as coded in the driver files.


### -field dwlDriverVersion

Version number of the driver. This comes out of the version structure of the driver.


### -field pszMfgName

Pointer to a null-terminated string that specifies the manufacturer's name.


### -field pszOEMUrl

Pointer to a null-terminated string that specifies the URL for the manufacturer.


### -field pszHardwareID

Pointer to a null-terminated string that specifies the hardware ID for the printer driver.


### -field pszProvider

Pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000")


## -remarks



The strings for these members are contained in the .inf file that is used to add the driver.

If you call <a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a> or <a href="https://msdn.microsoft.com/472adb7d-39cc-4c76-b96c-610ff9d276ad">AddPrinterDriverEx</a> with <i>Level</i> not equal to 6, and then you call <a href="https://msdn.microsoft.com/93f859b4-1005-4359-8029-9536d6eeb7e7">GetPrinterDriver</a> or <a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a> with <i>Level</i> equal to 6, the <b>DRIVER_INFO_6</b> structure is returned with <b>pszMfgName</b>, <b>pszOEMUrl</b>, <b>pszHardwareID</b>, and <b>pszProvider</b> set to <b>NULL</b>, <b>dwlDriverVersion</b> set to 0, and <b>ftDriverDate</b> set to (0,0).




## -see-also




<a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>



<a href="https://msdn.microsoft.com/472adb7d-39cc-4c76-b96c-610ff9d276ad">AddPrinterDriverEx</a>



<a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a>



<a href="https://msdn.microsoft.com/93f859b4-1005-4359-8029-9536d6eeb7e7">GetPrinterDriver</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

