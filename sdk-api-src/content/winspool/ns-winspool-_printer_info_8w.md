---
UID: NS:winspool._PRINTER_INFO_8W
title: "_PRINTER_INFO_8W"
author: windows-driver-content
description: The PRINTER_INFO_8 structure specifies the global default printer settings.
old-location: gdi\printer_info_8.htm
old-project: printdocs
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_INFO_8W, *PPRINTER_INFO_8W, PPRINTER_INFO_8, PPRINTER_INFO_8 structure pointer [Windows GDI], PRINTER_INFO_8, PRINTER_INFO_8 structure [Windows GDI], PRINTER_INFO_8W, _PRINTER_INFO_8A, _PRINTER_INFO_8W, _win32_PRINTER_INFO_8_str, gdi.printer_info_8, winspool/PPRINTER_INFO_8, winspool/PRINTER_INFO_8, winspool/_PRINTER_INFO_8A, winspool/_PRINTER_INFO_8W"
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
req.unicode-ansi: "_PRINTER_INFO_8W (Unicode) and _PRINTER_INFO_8A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_INFO_8W, *PPRINTER_INFO_8W, *LPPRINTER_INFO_8W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_INFO_8
-	_PRINTER_INFO_8A
-	_PRINTER_INFO_8W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_INFO_8W structure


## -description



The <b>PRINTER_INFO_8</b> structure specifies the global default printer settings.




## -struct-fields




### -field pDevMode

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that defines the global default printer data such as the paper orientation and the resolution.


## -remarks



The global defaults are set by the administrator of a printer that can be used by anyone. In contrast, the per-user defaults will affect a particular user or anyone else who uses the profile. For per-user defaults, use <a href="https://msdn.microsoft.com/8bafb995-f31c-46e3-a950-45e240c678aa">PRINTER_INFO_9</a>.




## -see-also




<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/8bafb995-f31c-46e3-a950-45e240c678aa">PRINTER_INFO_9</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

