---
UID: NS:winspool._PRINTER_NOTIFY_OPTIONS
title: "_PRINTER_NOTIFY_OPTIONS"
author: windows-driver-content
description: The PRINTER_NOTIFY_OPTIONS structure specifies options for a change notification object that monitors a printer or print server.
old-location: gdi\printer_notify_options.htm
old-project: printdocs
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS, PPRINTER_NOTIFY_OPTIONS, PPRINTER_NOTIFY_OPTIONS structure pointer [Windows GDI], PRINTER_NOTIFY_OPTIONS, PRINTER_NOTIFY_OPTIONS structure [Windows GDI], _PRINTER_NOTIFY_OPTIONS, _win32_PRINTER_NOTIFY_OPTIONS_str, gdi.printer_notify_options, winspool/PPRINTER_NOTIFY_OPTIONS, winspool/PRINTER_NOTIFY_OPTIONS"
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS, *LPPRINTER_NOTIFY_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_NOTIFY_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_NOTIFY_OPTIONS structure


## -description



The <b>PRINTER_NOTIFY_OPTIONS</b> structure specifies options for a change notification object that monitors a printer or print server.




## -struct-fields




### -field Version

The version of this structure. Set this member to 2.


### -field Flags

A bit flag. If you set the PRINTER_NOTIFY_OPTIONS_REFRESH flag in a call to the <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function, the function provides current data for all monitored printer information fields. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> function ignores the <b>Flags</b> member.


### -field Count

The number of elements in the <b>pTypes</b> array.


### -field pTypes

A pointer to an array of <a href="https://msdn.microsoft.com/1009f892-d3a8-4887-99b4-a35d1268eeb4">PRINTER_NOTIFY_OPTIONS_TYPE</a> structures. Use one element of this array to specify the printer information fields to monitor, and one element to specify the job information fields to monitor. You can monitor either printer information, job information, or both.


## -remarks



Use this structure with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> function to specify the set of printer or job information fields to monitor for change.

Use this structure with the <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function to request the current data for all monitored printer and job information fields. In this case, the <b>Flags</b> member specifies the PRINTER_NOTIFY_OPTIONS_REFRESH flag, and the function ignores the other structure members.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/1009f892-d3a8-4887-99b4-a35d1268eeb4">PRINTER_NOTIFY_OPTIONS_TYPE</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

