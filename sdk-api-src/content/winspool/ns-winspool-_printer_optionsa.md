---
UID: NS:winspool._PRINTER_OPTIONSA
title: "_PRINTER_OPTIONSA"
author: windows-driver-content
description: Represents printer options.
old-location: gdi\printer_options.htm
old-project: printdocs
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_OPTIONSA, *PPRINTER_OPTIONSA, PPRINTER_OPTIONS, PPRINTER_OPTIONS structure pointer [Windows GDI], PRINTER_OPTIONS, PRINTER_OPTIONS structure [Windows GDI], PRINTER_OPTIONSA, _PRINTER_OPTIONSA, _PRINTER_OPTIONSW, _win32_PRINTER_OPTIONS_str, gdi.printer_options, winspool/PPRINTER_OPTIONS, winspool/PRINTER_OPTIONS"
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_OPTIONSA, *PPRINTER_OPTIONSA, *LPPRINTER_OPTIONSA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_OPTIONSA structure


## -description



Represents printer options.




## -struct-fields




### -field cbSize

The size of the <b>PRINTER_OPTIONS</b> structure.


### -field dwFlags

A set of <a href="https://msdn.microsoft.com/e5a62322-723c-490d-8de1-f74dcac9e22d">PRINTER_OPTION_FLAGS</a> that specifies how the handle to a printer returned by <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a> will be used by other functions.


## -see-also




<a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a>



<a href="https://msdn.microsoft.com/e5a62322-723c-490d-8de1-f74dcac9e22d">PRINTER_OPTION_FLAGS</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

