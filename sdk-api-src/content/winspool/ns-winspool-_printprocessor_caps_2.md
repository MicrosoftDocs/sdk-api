---
UID: NS:winspool._PRINTPROCESSOR_CAPS_2
title: "_PRINTPROCESSOR_CAPS_2"
author: windows-driver-content
description: Represents printer capability information.
old-location: gdi\printprocessor_caps_2.htm
old-project: printdocs
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PPRINTPROCESSOR_CAPS_2, PPRINTPROCESSOR_CAPS_2, PPRINTPROCESSOR_CAPS_2 structure pointer [Windows GDI], PRINTPROCESSOR_CAPS_2, PRINTPROCESSOR_CAPS_2 structure [Windows GDI], _PRINTPROCESSOR_CAPS_2, _win32_PRINTPROCESSOR_CAPS_2_str, gdi.printprocessor_caps_2, winspool/PPRINTPROCESSOR_CAPS_2, winspool/PRINTPROCESSOR_CAPS_2"
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
req.typenames: PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTPROCESSOR_CAPS_2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTPROCESSOR_CAPS_2 structure


## -description



Represents printer capability information.




## -struct-fields




### -field dwLevel

A value that indicates the structure's version number.


### -field dwNupOptions

A bit mask representing the various numbers of document pages the printer can print on a single side of a physical sheet. The least significant bit represents one document page per side, the next bit represents 2 document pages per side, and so on. For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical side.


### -field dwPageOrderFlags

A flag value that indicates the order in which pages will be printed. It can be <b>NORMAL_PRINT</b>, <b>REVERSE_PRINT</b>, or <b>BOOKLET_PRINT</b>.


### -field dwNumberOfCopies

The maximum number of copies the printer can handle.


### -field dwDuplexHandlingCaps

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PPCAPS_REVERSE_PAGES_FOR_REVERSE_DUPLEX</td>
<td>When printing in reverse order and duplexing, the processor can print swap the order of each pair of pages, so instead of printing in order 4,3,2,1, they will print in the order 3,4,1,2.</td>
</tr>
<tr>
<td>PPCAPS_DONT_SEND_EXTRA_PAGES_FOR_DUPLEX</td>
<td>When duplexing, the Print Processor can be told not to send an extra page when there is an odd number of document pages. The processor will honor the value as best as it can, but in cases where preventing an extra blank page would cause improper output, the extra pages may still be sent.</td>
</tr>
</table>
 


### -field dwNupDirectionCaps

The available patterns when multiple document pages are printed on the same side of a sheet of paper. The possible flags are the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PPCAPS_RIGHT_THEN_DOWN</td>
<td>Pages appear in rows from right to left, each subsequent row below its predecessor.</td>
</tr>
<tr>
<td>PPCAPS_DOWN_THEN_RIGHT</td>
<td>Pages appear in columns from top to bottom, each subsequent column to the right of its predecessor.</td>
</tr>
<tr>
<td>PPCAPS_LEFT_THEN_DOWN</td>
<td>Pages appear in rows from left to right, each subsequent row below its predecessor.</td>
</tr>
<tr>
<td>PPCAPS_DOWN_THEN_LEFT</td>
<td>Pages appear in columns from top to bottom, each subsequent column to the left of its predecessor.</td>
</tr>
</table>
 


### -field dwNupBorderCaps

Can be only PPCAPS_BORDER_PRINT, indicating that, when multiple document pages are being printed on a single side of a physical sheet, the printer can be told whether or not to print a border around the imageable area of each document page.


### -field dwBookletHandlingCaps

Can only be PPCAPS_BOOKLET_EDGE, indicating that the printer can print booklet style.


### -field dwScalingCaps

Can only be PPCAPS_SQUARE_SCALING, indicating that the printer can scale the page image.


## -remarks



Values for all structure members are supplied by the <b>GetPrintProcessorCapabilities</b> function which is documented in the Windows Driver Kit.

When an application calls <a href="https://msdn.microsoft.com/b5a44b27-a4aa-4e58-9a64-05be87d12ab5">GetPrinterData</a>, the spooler calls a print processor's <b>GetPrintProcessorCapabilities</b> function and specifies a value name that has a format of <b>PrintProcCaps_</b><i>datatype</i>, where <i>datatype</i> is the name of an input data type.




## -see-also




<a href="https://msdn.microsoft.com/b5a44b27-a4aa-4e58-9a64-05be87d12ab5">GetPrinterData</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

