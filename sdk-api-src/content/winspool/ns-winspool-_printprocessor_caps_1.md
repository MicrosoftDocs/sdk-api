---
UID: NS:winspool._PRINTPROCESSOR_CAPS_1
title: "_PRINTPROCESSOR_CAPS_1"
author: windows-driver-content
description: The PRINTPROCESSOR_CAPS_1 structure is the format for the printer capability information that is returned by the GetPrinterData function in the buffer specified by the pData variable.
old-location: gdi\printprocessor_caps_1.htm
old-project: printdocs
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PPRINTPROCESSOR_CAPS_1, PPRINTPROCESSOR_CAPS_1, PPRINTPROCESSOR_CAPS_1 structure pointer [Windows GDI], PRINTPROCESSOR_CAPS_1, PRINTPROCESSOR_CAPS_1 structure [Windows GDI], _PRINTPROCESSOR_CAPS_1, _win32_PRINTPROCESSOR_CAPS_1_str, gdi.printprocessor_caps_1, winspool/PPRINTPROCESSOR_CAPS_1, winspool/PRINTPROCESSOR_CAPS_1"
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
req.typenames: PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTPROCESSOR_CAPS_1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTPROCESSOR_CAPS_1 structure


## -description



The <b>PRINTPROCESSOR_CAPS_1</b> structure is the format for the printer capability information that is returned by the <a href="https://msdn.microsoft.com/b5a44b27-a4aa-4e58-9a64-05be87d12ab5">GetPrinterData</a> function in the buffer specified by the <i>pData</i> variable.




## -struct-fields




### -field dwLevel

The structure's version number. This value must be 1.


### -field dwNupOptions

A bit mask representing the various numbers of document pages the printer can print on a physical page. The least significant bit represents 1 document page per page, the next bit represents 2 document pages per page, and so on. For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical page.


### -field dwPageOrderFlags

The order in which pages will be printed. This value can be NORMAL_PRINT, REVERSE_PRINT, or BOOKLET_PRINT.


### -field dwNumberOfCopies

The maximum number of copies the printer can handle.


## -remarks



Values for all structure members are supplied by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550522">GetPrintProcessorCapabilities</a> function, which is documented in the Windows Driver Kit (WDK).

The spooler calls a print processor's <a href="https://msdn.microsoft.com/library/windows/hardware/ff550522">GetPrintProcessorCapabilities</a> function when an application calls <a href="https://msdn.microsoft.com/b5a44b27-a4aa-4e58-9a64-05be87d12ab5">GetPrinterData</a>, specifying a value name with a format of PrintProcCaps_<i>datatype</i>, where <i>datatype</i> is the name of an input data type.




## -see-also




<a href="https://msdn.microsoft.com/b5a44b27-a4aa-4e58-9a64-05be87d12ab5">GetPrinterData</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

