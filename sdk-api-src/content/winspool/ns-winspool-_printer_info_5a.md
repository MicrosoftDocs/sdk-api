---
UID: NS:winspool._PRINTER_INFO_5A
title: "_PRINTER_INFO_5A"
author: windows-driver-content
description: The PRINTER_INFO_5 structure specifies detailed printer information.
old-location: gdi\printer_info_5.htm
old-project: printdocs
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_INFO_5A, *PPRINTER_INFO_5A, PPRINTER_INFO_5, PPRINTER_INFO_5 structure pointer [Windows GDI], PRINTER_INFO_5, PRINTER_INFO_5 structure [Windows GDI], PRINTER_INFO_5A, _PRINTER_INFO_5A, _PRINTER_INFO_5W, _win32_PRINTER_INFO_5_str, gdi.printer_info_5, winspool/PPRINTER_INFO_5, winspool/PRINTER_INFO_5, winspool/_PRINTER_INFO_5A, winspool/_PRINTER_INFO_5W"
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
req.unicode-ansi: "_PRINTER_INFO_5W (Unicode) and _PRINTER_INFO_5A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_INFO_5A, *PPRINTER_INFO_5A, *LPPRINTER_INFO_5A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_INFO_5
-	_PRINTER_INFO_5A
-	_PRINTER_INFO_5W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_INFO_5A structure


## -description



The <b>PRINTER_INFO_5</b> structure specifies detailed printer information.




## -struct-fields




### -field pPrinterName

A pointer to a null-terminated string that specifies the name of the printer.


### -field pPortName

A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer. If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").


### -field Attributes

The printer attributes. This member can be any reasonable combination of the following values.<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_DIRECT</td>
<td>Job is sent directly to the printer (it is not spooled).</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST</td>
<td>If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_ENABLE_DEVQ</td>
<td>If set, <b>DevQueryPrint</b> is called. <b>DevQueryPrint</b> may fail if the document and printer setups do not match. Setting this flag causes mismatched documents to be held in the queue.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_HIDDEN</td>
<td>Reserved.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS</td>
<td>If set, jobs are kept after they are printed. If unset, jobs are deleted.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_LOCAL</td>
<td>Printer is a local printer.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_NETWORK</td>
<td>Printer is a network printer connection.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_PUBLISHED</td>
<td> Indicates whether the printer is published in the directory service.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_QUEUED</td>
<td>If set, the printer spools and starts printing after the last page is spooled. If not set and PRINTER_ATTRIBUTE_DIRECT is not set, the printer spools and prints while spooling.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_RAW_ONLY</td>
<td>Indicates that only raw data type print jobs can be spooled.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_SHARED</td>
<td>Printer is shared.</td>
</tr>
</table>
 



In Windows XP and later versions of Windows, the following value can also be used.<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_FAX</td>
<td> If set, printer is a fax printer. This can only be set by <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a>, but it can be retrieved by <a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a> and <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>.</td>
</tr>
</table>
 



In Windows Vista and later versions of Windows, the following values can also be used.<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_FRIENDLY_NAME</td>
<td> A computer has connected to this printer and given it a friendly name.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_MACHINE</td>
<td> Printer is a per-machine connection.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_PUSHED_USER</td>
<td> The printer was installed by using the Push Printer Connections user policy. </td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_PUSHED_MACHINE</td>
<td> The printer was installed by using the Push Printer Connections computer policy. </td>
</tr>
</table>
 




### -field DeviceNotSelectedTimeout

 This value is not used.


### -field TransmissionRetryTimeout

 This value is not used.


## -see-also




<a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a>



<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/527d635d-2d75-4b56-bab7-e95c9919a8fb">PRINTER_INFO_3</a>



<a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

