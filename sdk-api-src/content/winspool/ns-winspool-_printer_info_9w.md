---
UID: NS:winspool._PRINTER_INFO_9W
title: "_PRINTER_INFO_9W"
author: windows-driver-content
description: The PRINTER_INFO_9 structure specifies the per-user default printer settings.
old-location: gdi\printer_info_9.htm
old-project: printdocs
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_INFO_9W, *PPRINTER_INFO_9W, PPRINTER_INFO_9, PPRINTER_INFO_9 structure pointer [Windows GDI], PRINTER_INFO_9, PRINTER_INFO_9 structure [Windows GDI], PRINTER_INFO_9W, _PRINTER_INFO_9A, _PRINTER_INFO_9W, _win32_PRINTER_INFO_9_str, gdi.printer_info_9, winspool/PPRINTER_INFO_9, winspool/PRINTER_INFO_9, winspool/_PRINTER_INFO_9A, winspool/_PRINTER_INFO_9W"
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
req.unicode-ansi: "_PRINTER_INFO_9W (Unicode) and _PRINTER_INFO_9A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_INFO_9W, *PPRINTER_INFO_9W, *LPPRINTER_INFO_9W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_INFO_9
-	_PRINTER_INFO_9A
-	_PRINTER_INFO_9W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_INFO_9W structure


## -description



The <b>PRINTER_INFO_9</b> structure specifies the per-user default printer settings.




## -struct-fields




### -field pDevMode

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that defines the per-user default printer data such as the paper orientation and the resolution. The <b>DEVMODE</b> is stored in the user's registry.


## -remarks



The per-user defaults will affect only a particular user or anyone who uses the profile. In contrast, the global defaults are set by the administrator of a printer that can be used by anyone. For global defaults, use <a href="https://msdn.microsoft.com/98f26a45-5302-4358-bed6-691d9bc37554">PRINTER_INFO_8</a>.




## -see-also




<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/98f26a45-5302-4358-bed6-691d9bc37554">PRINTER_INFO_8</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

