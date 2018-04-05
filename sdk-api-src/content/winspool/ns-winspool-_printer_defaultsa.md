---
UID: NS:winspool._PRINTER_DEFAULTSA
title: "_PRINTER_DEFAULTSA"
author: windows-driver-content
description: The PRINTER_DEFAULTS structure specifies the default data type, environment, initialization data, and access rights for a printer.
old-location: gdi\printer_defaults.htm
old-project: printdocs
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_DEFAULTSA, *PPRINTER_DEFAULTSA, PPRINTER_DEFAULTS, PPRINTER_DEFAULTS structure pointer [Windows GDI], PRINTER_DEFAULTS, PRINTER_DEFAULTS structure [Windows GDI], PRINTER_DEFAULTSA, _PRINTER_DEFAULTSA, _PRINTER_DEFAULTSW, _win32_PRINTER_DEFAULTS_str, gdi.printer_defaults, winspool/PPRINTER_DEFAULTS, winspool/PRINTER_DEFAULTS, winspool/_PRINTER_DEFAULTSA, winspool/_PRINTER_DEFAULTSW"
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
req.unicode-ansi: "_PRINTER_DEFAULTSW (Unicode) and _PRINTER_DEFAULTSA (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_DEFAULTSA, *PPRINTER_DEFAULTSA, *LPPRINTER_DEFAULTSA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_DEFAULTS
-	_PRINTER_DEFAULTSA
-	_PRINTER_DEFAULTSW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_DEFAULTSA structure


## -description



The <b>PRINTER_DEFAULTS</b> structure specifies the default data type, environment, initialization data, and access rights for a printer.




## -struct-fields




### -field pDatatype

Pointer to a null-terminated string that specifies the default data type for a printer.


### -field pDevMode

Pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that identifies the default environment and initialization data for a printer.


### -field DesiredAccess


             Specifies desired access rights for a printer. The <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> function uses this member to set access rights to the printer. These rights can affect the operation of the <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> and <a href="https://msdn.microsoft.com/04d9c073-b795-4307-ba89-d4984bc5b354">DeletePrinter</a> functions. The access rights can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PRINTER_ACCESS_ADMINISTER</td>
<td>To perform administrative tasks, such as those provided by <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>.</td>
</tr>
<tr>
<td>PRINTER_ACCESS_USE</td>
<td>To perform basic printing operations.</td>
</tr>
<tr>
<td>PRINTER_ACCESS_MANAGE_LIMITED</td>
<td>To perform administrative tasks, such as those provided by <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> and <a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a>. This value is available starting from Windows 8.1.</td>
</tr>
<tr>
<td>PRINTER_ALL_ACCESS</td>
<td>To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a> ).</td>
</tr>
<tr>
<td>generic security values, such as WRITE_DAC</td>
<td>To allow specific control access rights. See <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a>.</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/04d9c073-b795-4307-ba89-d4984bc5b354">DeletePrinter</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

