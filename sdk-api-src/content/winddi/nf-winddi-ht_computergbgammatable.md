---
UID: NF:winddi.HT_ComputeRGBGammaTable
title: HT_ComputeRGBGammaTable function (winddi.h)
description: The HT_ComputeRGBGammaTable function causes GDI to compute device red, green, and blue intensities based on gamma numbers.
helpviewer_keywords: ["HT_ComputeRGBGammaTable","HT_ComputeRGBGammaTable function [Display Devices]","display.ht_computergbgammatable","gdifncs_10a08358-3fbf-4684-8dd6-c126e14310f5.xml","winddi/HT_ComputeRGBGammaTable"]
old-location: display\ht_computergbgammatable.htm
tech.root: display
ms.assetid: 63496600-9627-432b-a86e-1069ccd21f49
ms.date: 12/05/2018
ms.keywords: HT_ComputeRGBGammaTable, HT_ComputeRGBGammaTable function [Display Devices], display.ht_computergbgammatable, gdifncs_10a08358-3fbf-4684-8dd6-c126e14310f5.xml, winddi/HT_ComputeRGBGammaTable
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HT_ComputeRGBGammaTable
 - winddi/HT_ComputeRGBGammaTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - HT_ComputeRGBGammaTable
---

# HT_ComputeRGBGammaTable function


## -description

The <b>HT_ComputeRGBGammaTable</b> function causes GDI to compute device red, green, and blue intensities based on gamma numbers.

## -parameters

### -param GammaTableEntries [in]

Specifies the total number of steps in the table for each of red, green, and blue intensities. This value must greater than 1 and less than or equal to 256 (that is, 2 &lt;= <i>GammaTableEntries</i> &lt;= 256). For example, a value of 256 means there are 256 red entries, 256 green entries, and 256 blue entries in the gamma table.

### -param GammaTableType [in]

Specifies <i>pGammaTable</i>'s organization. Valid table types are:

<table>
<tr>
<th>GammaTableType</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
The gamma table's red, green, and blue values are interleaved together. Each gamma step is 3 bytes; 1 byte each for red, green, and blue. 

</td>
</tr>
<tr>
<td>
1

</td>
<td>
The red, green, and blue tables are packed separately; that is, the entire red table is followed by the entire green table, which is followed by the entire blue table. Individual entries are 1 byte each, making each subtable a total of <i>GammaTableEntries</i> bytes in length.

</td>
</tr>
</table>

### -param RedGamma [in]

Specifies the red gamma value. This USHORT value is interpreted as a real number whose four least-significant digits are to the right of the (implied) decimal point. For example, a gamma value of 10000 represents the real number 1.0000, and 12345 represents 1.2345. The minimum gamma value allowed is 0.0000, and the maximum allowable value is 6.5535.

### -param GreenGamma [in]

Specifies the green gamma value. This USHORT value is interpreted as a real number whose four least-significant digits are to the right of the (implied) decimal point. For example, a gamma value of 10000 represents the real number 1.0000, and 12345 represents 1.2345. The minimum gamma value allowed is 0.0000, and the maximum allowable value is 6.5535.

### -param BlueGamma [in]

Specifies the blue gamma value. This USHORT value is interpreted as a real number whose four least-significant digits are to the right of the (implied) decimal point. For example, a gamma value of 10000 represents the real number 1.0000, and 12345 represents 1.2345. The minimum gamma value allowed is 0.0000, and the maximum allowable value is 6.5535.

### -param pGammaTable [out]

Pointer to the array of bytes in which the gamma table's red, green, and blue intensities will be written. The returned table is organized as specified by the <i>GammaTableType</i> parameter.

## -returns

The return value is the number of gamma entries written to <i>pGammaTable</i>; upon success, this value is equal to <i>GammaTableEntries</i>. If <i>GammaTableEntries</i> is less than 2 or greater than 256, the return value is 0.

The red, green, and blue intensities returned in <i>pGammaTable</i> range from 0 to 255.

## -remarks

GDI halftone service routines use a special palette to do halftoning. If the device selects an 8-bit per pixel palette from a pool of 24-bit device colors for a 16-bit or 24-bit type surface, GDI assumes red, green, and blue color steps; each has equal brightness.

GDI provides this service so that the driver can query the 8-bit per pixel halftone palette used by GDI or compute gamma corrected and equalized RGB color intensities for the device.
