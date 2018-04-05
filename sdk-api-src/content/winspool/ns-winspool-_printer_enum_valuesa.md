---
UID: NS:winspool._PRINTER_ENUM_VALUESA
title: "_PRINTER_ENUM_VALUESA"
author: windows-driver-content
description: The PRINTER_ENUM_VALUES structure specifies the value name, type, and data for a printer configuration value returned by the EnumPrinterDataEx function.
old-location: gdi\printer_enum_values.htm
old-project: printdocs
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_ENUM_VALUESA, *PPRINTER_ENUM_VALUESA, PPRINTER_ENUM_VALUES, PPRINTER_ENUM_VALUES structure pointer [Windows GDI], PRINTER_ENUM_VALUES, PRINTER_ENUM_VALUES structure [Windows GDI], PRINTER_ENUM_VALUESA, _PRINTER_ENUM_VALUESA, _PRINTER_ENUM_VALUESW, _win32_PRINTER_ENUM_VALUES_str, gdi.printer_enum_values, winspool/PPRINTER_ENUM_VALUES, winspool/PRINTER_ENUM_VALUES, winspool/_PRINTER_ENUM_VALUESA, winspool/_PRINTER_ENUM_VALUESW"
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
req.unicode-ansi: "_PRINTER_ENUM_VALUESW (Unicode) and _PRINTER_ENUM_VALUESA (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_ENUM_VALUESA, *PPRINTER_ENUM_VALUESA, *LPPRINTER_ENUM_VALUESA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_ENUM_VALUES
-	_PRINTER_ENUM_VALUESA
-	_PRINTER_ENUM_VALUESW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_ENUM_VALUESA structure


## -description



The <b>PRINTER_ENUM_VALUES</b> structure specifies the value name, type, and data for a printer configuration value returned by the <a href="https://msdn.microsoft.com/bc5ecc46-24a4-4b54-9431-0eaf6446e2d6">EnumPrinterDataEx</a> function.




## -struct-fields




### -field pValueName

Pointer to a null-terminated string that specifies the name of the retrieved value.


### -field cbValueName

The number of bytes in the <b>pValueName</b> member, including the terminating NULL character.


### -field dwType

A code indicating the type of data pointed to by the <b>pData</b> member. For a list of the possible type codes, see <a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>.


### -field pData

Pointer to a buffer containing the data for the retrieved value.


### -field cbData

The number of bytes retrieved in the <b>pData</b> buffer.


## -see-also




<a href="https://msdn.microsoft.com/bc5ecc46-24a4-4b54-9431-0eaf6446e2d6">EnumPrinterDataEx</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

