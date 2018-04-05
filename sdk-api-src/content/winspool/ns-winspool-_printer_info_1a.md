---
UID: NS:winspool._PRINTER_INFO_1A
title: "_PRINTER_INFO_1A"
author: windows-driver-content
description: The PRINTER_INFO_1 structure specifies general printer information.
old-location: gdi\printer_info_1.htm
old-project: printdocs
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_INFO_1A, *PPRINTER_INFO_1A, PPRINTER_INFO_1, PPRINTER_INFO_1 structure pointer [Windows GDI], PRINTER_INFO_1, PRINTER_INFO_1 structure [Windows GDI], PRINTER_INFO_1A, _PRINTER_INFO_1A, _PRINTER_INFO_1W, _win32_PRINTER_INFO_1_str, gdi.printer_info_1, winspool/PPRINTER_INFO_1, winspool/PRINTER_INFO_1, winspool/_PRINTER_INFO_1A, winspool/_PRINTER_INFO_1W"
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
req.unicode-ansi: "_PRINTER_INFO_1W (Unicode) and _PRINTER_INFO_1A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_INFO_1A, *PPRINTER_INFO_1A, *LPPRINTER_INFO_1A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_INFO_1
-	_PRINTER_INFO_1A
-	_PRINTER_INFO_1W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_INFO_1A structure


## -description



The <b>PRINTER_INFO_1</b> structure specifies general printer information.




## -struct-fields




### -field Flags

Specifies information about the returned data. Following are the values for this member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PRINTER_ENUM_EXPAND</td>
<td>A print provider can set this flag as a hint to a calling application to enumerate this object further if default expansion is enabled. For example, when domains are enumerated, a print provider might indicate the user's domain by setting this flag.</td>
</tr>
<tr>
<td>PRINTER_ENUM_CONTAINER</td>
<td>If this flag is set, the printer object may contain enumerable objects. For example, the object may be a print server that contains printers.</td>
</tr>
<tr>
<td>PRINTER_ENUM_ICON1</td>
<td>Indicates that, where appropriate, an application should display an icon identifying the object as a top-level network name, such as Microsoft Windows Network.</td>
</tr>
<tr>
<td>PRINTER_ENUM_ICON2</td>
<td>Indicates that, where appropriate, an application should display an icon that identifies the object as a network domain.</td>
</tr>
<tr>
<td>PRINTER_ENUM_ICON3</td>
<td>Indicates that, where appropriate, an application should display an icon that identifies the object as a print server.</td>
</tr>
<tr>
<td>PRINTER_ENUM_ICON4</td>
<td>Reserved.</td>
</tr>
<tr>
<td>PRINTER_ENUM_ICON5</td>
<td>Reserved.</td>
</tr>
<tr>
<td>PRINTER_ENUM_ICON6</td>
<td>Reserved.</td>
</tr>
<tr>
<td>PRINTER_ENUM_ICON7</td>
<td>Reserved.</td>
</tr>
<tr>
<td>PRINTER_ENUM_ICON8</td>
<td>Indicates that, where appropriate, an application should display an icon that identifies the object as a printer.</td>
</tr>
</table>
 


### -field pDescription


             Pointer to a null-terminated string that describes the contents of the structure.


### -field pName


             Pointer to a null-terminated string that names the contents of the structure.


### -field pComment


             Pointer to a null-terminated string that contains additional data describing the structure.


## -see-also




<a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a>



<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/527d635d-2d75-4b56-bab7-e95c9919a8fb">PRINTER_INFO_3</a>



<a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

