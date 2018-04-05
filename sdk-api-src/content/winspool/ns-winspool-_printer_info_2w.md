---
UID: NS:winspool._PRINTER_INFO_2W
title: "_PRINTER_INFO_2W"
author: windows-driver-content
description: The PRINTER_INFO_2 structure specifies detailed printer information.
old-location: gdi\printer_info_2.htm
old-project: printdocs
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_INFO_2W, *PPRINTER_INFO_2W, PPRINTER_INFO_2, PPRINTER_INFO_2 structure pointer [Windows GDI], PRINTER_INFO_2, PRINTER_INFO_2 structure [Windows GDI], PRINTER_INFO_2W, _PRINTER_INFO_2A, _PRINTER_INFO_2W, _win32_PRINTER_INFO_2_str, gdi.printer_info_2, winspool/PPRINTER_INFO_2, winspool/PRINTER_INFO_2, winspool/_PRINTER_INFO_2A, winspool/_PRINTER_INFO_2W"
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
req.unicode-ansi: "_PRINTER_INFO_2W (Unicode) and _PRINTER_INFO_2A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_INFO_2W, *PPRINTER_INFO_2W, *LPPRINTER_INFO_2W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_INFO_2
-	_PRINTER_INFO_2A
-	_PRINTER_INFO_2W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_INFO_2W structure


## -description



The <b>PRINTER_INFO_2</b> structure specifies detailed printer information.




## -struct-fields




### -field pServerName

A pointer to a null-terminated string identifying the server that controls the printer. If this string is <b>NULL</b>, the printer is controlled locally.


### -field pPrinterName

A pointer to a null-terminated string that specifies the name of the printer.


### -field pShareName

A pointer to a null-terminated string that identifies the share point for the printer. (This string is used only if the PRINTER_ATTRIBUTE_SHARED constant was set for the <b>Attributes</b> member.)


### -field pPortName

A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer. If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").


### -field pDriverName

A pointer to a null-terminated string that specifies the name of the printer driver.


### -field pComment

A pointer to a null-terminated string that provides a brief description of the printer.


### -field pLocation

A pointer to a null-terminated string that specifies the physical location of the printer (for example, "Bldg. 38, Room 1164").


### -field pDevMode

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that defines default printer data such as the paper orientation and the resolution.


### -field pSepFile

A pointer to a null-terminated string that specifies the name of the file used to create the separator page. This page is used to separate print jobs sent to the printer.


### -field pPrintProcessor

A pointer to a null-terminated string that specifies the name of the print processor used by the printer. You can use the <a href="https://msdn.microsoft.com/98c9185c-c89d-4b4e-8c1e-7e22b315f188">EnumPrintProcessors</a> function to obtain a list of print processors installed on a server.


### -field pDatatype

A pointer to a null-terminated string that specifies the data type used to record the print job. You can use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548757">EnumPrintProcessorDatatypes</a> function to obtain a list of data types supported by a specific print processor.


### -field pParameters

A pointer to a null-terminated string that specifies the default print-processor parameters.


### -field pSecurityDescriptor

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure for the printer. This member may be <b>NULL</b>.


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
 



In Windows Server 2003, the following value can also be used.<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_TS</td>
<td> Indicates the printer is currently connected through a terminal server.</td>
</tr>
</table>
 




### -field Priority

A priority value that the spooler uses to route print jobs.


### -field DefaultPriority

The default priority value assigned to each print job.


### -field StartTime

The earliest time at which the printer will print a job. This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).


### -field UntilTime

The latest time at which the printer will print a job. This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).


### -field Status

The printer status. This member can be any reasonable combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PRINTER_STATUS_BUSY</td>
<td>The printer is busy.</td>
</tr>
<tr>
<td>PRINTER_STATUS_DOOR_OPEN</td>
<td>The printer door is open.</td>
</tr>
<tr>
<td>PRINTER_STATUS_ERROR</td>
<td>The printer is in an error state.</td>
</tr>
<tr>
<td>PRINTER_STATUS_INITIALIZING</td>
<td>The printer is initializing.</td>
</tr>
<tr>
<td>PRINTER_STATUS_IO_ACTIVE</td>
<td>The printer is in an active input/output state</td>
</tr>
<tr>
<td>PRINTER_STATUS_MANUAL_FEED</td>
<td>The printer is in a manual feed state.</td>
</tr>
<tr>
<td>PRINTER_STATUS_NO_TONER</td>
<td>The printer is out of toner.</td>
</tr>
<tr>
<td>PRINTER_STATUS_NOT_AVAILABLE</td>
<td>The printer is not available for printing.</td>
</tr>
<tr>
<td>PRINTER_STATUS_OFFLINE</td>
<td>The printer is offline.</td>
</tr>
<tr>
<td>PRINTER_STATUS_OUT_OF_MEMORY</td>
<td>The printer has run out of memory.</td>
</tr>
<tr>
<td>PRINTER_STATUS_OUTPUT_BIN_FULL</td>
<td>The printer's output bin is full.</td>
</tr>
<tr>
<td>PRINTER_STATUS_PAGE_PUNT</td>
<td>The printer cannot print the current page.</td>
</tr>
<tr>
<td>PRINTER_STATUS_PAPER_JAM</td>
<td>Paper is jammed in the printer</td>
</tr>
<tr>
<td>PRINTER_STATUS_PAPER_OUT</td>
<td>The printer is out of paper.</td>
</tr>
<tr>
<td>PRINTER_STATUS_PAPER_PROBLEM</td>
<td>The printer has a paper problem.</td>
</tr>
<tr>
<td>PRINTER_STATUS_PAUSED</td>
<td>The printer is paused.</td>
</tr>
<tr>
<td>PRINTER_STATUS_PENDING_DELETION</td>
<td>The printer is being deleted.</td>
</tr>
<tr>
<td>PRINTER_STATUS_POWER_SAVE</td>
<td>The printer is in power save mode.</td>
</tr>
<tr>
<td>PRINTER_STATUS_PRINTING</td>
<td>The printer is printing.</td>
</tr>
<tr>
<td>PRINTER_STATUS_PROCESSING</td>
<td>The printer is processing a print job.</td>
</tr>
<tr>
<td>PRINTER_STATUS_SERVER_UNKNOWN</td>
<td>The printer status is unknown.</td>
</tr>
<tr>
<td>PRINTER_STATUS_TONER_LOW</td>
<td>The printer is low on toner.</td>
</tr>
<tr>
<td>PRINTER_STATUS_USER_INTERVENTION</td>
<td>The printer has an error that requires the user to do something.</td>
</tr>
<tr>
<td>PRINTER_STATUS_WAITING</td>
<td>The printer is waiting.</td>
</tr>
<tr>
<td>PRINTER_STATUS_WARMING_UP</td>
<td>The printer is warming up.</td>
</tr>
</table>
 


### -field cJobs

The number of print jobs that have been queued for the printer.


### -field AveragePPM

The average number of pages per minute that have been printed on the printer.


## -see-also




<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a>



<a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a>



<a href="https://msdn.microsoft.com/527d635d-2d75-4b56-bab7-e95c9919a8fb">PRINTER_INFO_3</a>



<a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>
 

 

