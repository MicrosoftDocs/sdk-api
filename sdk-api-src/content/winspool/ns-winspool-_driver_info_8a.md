---
UID: NS:winspool._DRIVER_INFO_8A
title: "_DRIVER_INFO_8A"
author: windows-driver-content
description: Contains printer driver information.
old-location: gdi\driver_info_8.htm
old-project: printdocs
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPDRIVER_INFO_8A, *PDRIVER_INFO_8A, DRIVER_INFO_8, DRIVER_INFO_8 structure [Windows GDI], DRIVER_INFO_8A, LPDRIVER_INFO_8, LPDRIVER_INFO_8 structure pointer [Windows GDI], PDRIVER_INFO_8, PDRIVER_INFO_8 structure pointer [Windows GDI], _DRIVER_INFO_8A, _DRIVER_INFO_8W, _win32_DRIVER_INFO_8_str, gdi.driver_info_8, winspool/DRIVER_INFO_8, winspool/LPDRIVER_INFO_8, winspool/PDRIVER_INFO_8, winspool/_DRIVER_INFO_8A, winspool/_DRIVER_INFO_8W"
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
req.unicode-ansi: "_DRIVER_INFO_8W (Unicode) and _DRIVER_INFO_8A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRIVER_INFO_8A, *PDRIVER_INFO_8A, *LPDRIVER_INFO_8A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	DRIVER_INFO_8
-	_DRIVER_INFO_8A
-	_DRIVER_INFO_8W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DRIVER_INFO_8A structure


## -description



Contains printer driver information.




## -struct-fields




### -field cVersion

The operating system version for which the driver was written. The supported value is 3.


### -field pName

A pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).


### -field pEnvironment

A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64.


### -field pDriverPath

A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\DRIVERS\Pscript.dll).


### -field pDataFile

A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\DRIVERS\Qms810.ppd).


### -field pConfigFile

A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\DRIVERS\Pscrptui.dll).


### -field pHelpFile

A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\DRIVERS\Pscrptui.hlp).


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

The version number of the driver. This comes from the version structure of the driver.


### -field pszMfgName

A pointer to a null-terminated string that specifies the manufacturer's name.


### -field pszOEMUrl

A pointer to a null-terminated string that specifies the URL for the manufacturer.


### -field pszHardwareID

A pointer to a null-terminated string that specifies the hardware ID for the printer driver.


### -field pszProvider

A pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000").


### -field pszPrintProcessor

A pointer to a null-terminated string that specifies the print processor (for example, "WinPrint").


### -field pszVendorSetup

A pointer to a null-terminated string that specifies the vendor's driver setup DLL and entry point.


### -field pszzColorProfiles

A pointer to a null-terminated string that specifies the color profiles associated with the driver.


### -field pszInfPath

A pointer to a null-terminated string that specifies the path to the driver's .inf file in the driver store. (See Remarks.) This must be <b>NULL</b> if the DRIVER_INFO_8 is being passed to <a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a> or <a href="https://msdn.microsoft.com/472adb7d-39cc-4c76-b96c-610ff9d276ad">AddPrinterDriverEx</a>.


### -field dwPrinterDriverAttributes

Attribute flags for printer drivers. This must be 0 if the DRIVER_INFO_8 is being passed to <a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a> or <a href="https://msdn.microsoft.com/472adb7d-39cc-4c76-b96c-610ff9d276ad">AddPrinterDriverEx</a>. Otherwise, it can be any combination of the following flags:

<table>
<tr>
<th>Flag name/value</th>
<th>Meaning</th>
<th>Minimum OS</th>
</tr>
<tr>
<td>
PRINTER_DRIVER_PACKAGE_AWARE

0x00000001

</td>
<td>The printer driver is part of a driver package.</td>
<td>Windows Vista</td>
</tr>
<tr>
<td>
PRINTER_DRIVER_XPS

0x00000002

</td>
<td>The printer driver supports the Microsoft XPS format described in the <a href="http://msdn.microsoft.com/en-us/windows/hardware/gg463373.aspx">XML Paper Specification: Overview</a>, and also in <a href="http://msdn.microsoft.com/en-us/library/e81cbc09-ab05-4a32-ae4a-8ec57b436c43(v=prot.10)">Product Behavior, section <27></a>.</td>
<td>
Windows 8

Windows Server 2012

</td>
</tr>
<tr>
<td>
PRINTER_DRIVER_SANDBOX_ENABLED

0x00000004

</td>
<td>The printer driver is compatible with <a href="http://msdn.microsoft.com/en-us/library/831cd729-be7c-451e-b729-bd8d84ce4d24(v=prot.10)">printer driver isolation</a>. For more information, see <a href="http://msdn.microsoft.com/en-us/library/e81cbc09-ab05-4a32-ae4a-8ec57b436c43(v=prot.10)">Product Behavior, section <28></a>.</td>
<td>
Windows 7

Windows Server 2008 R2

</td>
</tr>
<tr>
<td>
PRINTER_DRIVER_CLASS

0x00000008

</td>
<td>The printer driver is a <a href="http://msdn.microsoft.com/en-us/library/831cd729-be7c-451e-b729-bd8d84ce4d24(v=prot.10)">class printer driver</a>.</td>
<td>
Windows 8

Windows Server 2012

</td>
</tr>
<tr>
<td>
PRINTER_DRIVER_DERIVED

0x00000010

</td>
<td>The printer driver is a <a href="http://msdn.microsoft.com/en-us/library/831cd729-be7c-451e-b729-bd8d84ce4d24(v=prot.10)">derived printer driver</a>.</td>
<td>
Windows 8

Windows Server 2012

</td>
</tr>
<tr>
<td>
PRINTER_DRIVER_NOT_SHAREABLE

0x00000020

</td>
<td>Printers using this printer driver cannot be shared.</td>
<td>
Windows 8

Windows Server 2012

</td>
</tr>
<tr>
<td>
PRINTER_DRIVER_CATEGORY_FAX

0x00000040

</td>
<td>The printer driver is intended for use with <a href="http://msdn.microsoft.com/en-us/library/831cd729-be7c-451e-b729-bd8d84ce4d24(v=prot.10)">fax printers</a>.</td>
<td>
Windows 8

Windows Server 2012

</td>
</tr>
<tr>
<td>
PRINTER_DRIVER_CATEGORY_FILE

0x00000080

</td>
<td>The printer driver is intended for use with <a href="http://msdn.microsoft.com/en-us/library/831cd729-be7c-451e-b729-bd8d84ce4d24(v=prot.10)">file printers</a>.</td>
<td>
Windows 8

Windows Server 2012

</td>
</tr>
<tr>
<td>
PRINTER_DRIVER_CATEGORY_VIRTUAL

0x00000100

</td>
<td>The printer driver is intended for use with <a href="http://msdn.microsoft.com/en-us/library/831cd729-be7c-451e-b729-bd8d84ce4d24(v=prot.10)">virtual printers</a>.</td>
<td>
Windows 8

Windows Server 2012

</td>
</tr>
<tr>
<td>
PRINTER_DRIVER_CATEGORY_SERVICE

0x00000200

</td>
<td>The printer driver is intended for use with <a href="http://msdn.microsoft.com/en-us/library/831cd729-be7c-451e-b729-bd8d84ce4d24(v=prot.10)">service printers</a>.</td>
<td>
Windows 8

Windows Server 2012

</td>
</tr>
<tr>
<td>
PRINTER_DRIVER_SOFT_RESET_REQUIRED

0x00000400

</td>
<td>Printers that use this printer driver should follow the guidelines outlined in the USB Device Class Definition. For more information, see <a href="http://msdn.microsoft.com/en-us/library/e81cbc09-ab05-4a32-ae4a-8ec57b436c43(v=prot.10)">Product Behavior, section <36></a></td>
<td>
Windows 8

Windows Server 2012

</td>
</tr>
</table>
 


### -field pszzCoreDriverDependencies

A pointer to a null-terminated multi-string that specifies all the core printer drivers that the driver depends on. This must be <b>NULL</b> if the <b>DRIVER_INFO_8</b> is being passed to <a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a> or <a href="https://msdn.microsoft.com/472adb7d-39cc-4c76-b96c-610ff9d276ad">AddPrinterDriverEx</a>.


### -field ftMinInboxDriverVerDate

The earliest allowed date of any drivers that shipped with Windows and on which this driver depends.


### -field dwlMinInboxDriverVerVersion

The earliest allowed version of any drivers that shipped with Windows and on which this driver depends.


## -remarks



The strings for these members are contained in the .inf file that is used to add the driver.




## -see-also




<a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>



<a href="https://msdn.microsoft.com/472adb7d-39cc-4c76-b96c-610ff9d276ad">AddPrinterDriverEx</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

