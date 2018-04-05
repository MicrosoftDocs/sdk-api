---
UID: NS:winspool._PRINTER_INFO_6
title: "_PRINTER_INFO_6"
author: windows-driver-content
description: The PRINTER_INFO_6 specifies the status value of a printer.
old-location: gdi\printer_info_6.htm
old-project: printdocs
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_INFO_6, *PPRINTER_INFO_6, PPRINTER_INFO_6, PPRINTER_INFO_6 structure pointer [Windows GDI], PRINTER_INFO_6, PRINTER_INFO_6 structure [Windows GDI], _PRINTER_INFO_6, _PRINTER_INFO_6A, _PRINTER_INFO_6W, _win32_PRINTER_INFO_6_str, gdi.printer_info_6, winspool/PPRINTER_INFO_6, winspool/PRINTER_INFO_6, winspool/_PRINTER_INFO_6A, winspool/_PRINTER_INFO_6W"
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
req.unicode-ansi: "_PRINTER_INFO_6W (Unicode) and _PRINTER_INFO_6A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_INFO_6, *PPRINTER_INFO_6, *LPPRINTER_INFO_6
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_INFO_6
-	_PRINTER_INFO_6A
-	_PRINTER_INFO_6W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_INFO_6 structure


## -description



The <b>PRINTER_INFO_6</b> specifies the status value of a printer.




## -struct-fields




### -field dwStatus

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
<td>Not used.</td>
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
<td>The printer is pending deletion as a result of a call to the <a href="https://msdn.microsoft.com/04d9c073-b795-4307-ba89-d4984bc5b354">DeletePrinter</a> function.</td>
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
<td>The printer is processing a command from the <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> function.</td>
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
 


## -see-also




<a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/527d635d-2d75-4b56-bab7-e95c9919a8fb">PRINTER_INFO_3</a>



<a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>



<a href="https://msdn.microsoft.com/c8599f2e-3b7c-4fde-a340-ca7d3ddaa106">PRINTER_INFO_5</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

