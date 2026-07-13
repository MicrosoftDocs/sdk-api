---
UID: NF:winddi.HT_Get8BPPMaskPalette
title: HT_Get8BPPMaskPalette function (winddi.h)
description: The HT_Get8BPPMaskPalette function returns a mask palette for an 8-bits-per-pixel device type.
helpviewer_keywords: ["HT_Get8BPPMaskPalette","HT_Get8BPPMaskPalette function [Display Devices]","display.ht_get8bppmaskpalette","gdifncs_5d4e6366-f721-442d-9666-12cadfef89b9.xml","winddi/HT_Get8BPPMaskPalette"]
old-location: display\ht_get8bppmaskpalette.htm
tech.root: display
ms.assetid: 46e9b3e1-e9a5-4c18-8595-6f883a790b01
ms.date: 12/05/2018
ms.keywords: HT_Get8BPPMaskPalette, HT_Get8BPPMaskPalette function [Display Devices], display.ht_get8bppmaskpalette, gdifncs_5d4e6366-f721-442d-9666-12cadfef89b9.xml, winddi/HT_Get8BPPMaskPalette
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
 - HT_Get8BPPMaskPalette
 - winddi/HT_Get8BPPMaskPalette
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
 - HT_Get8BPPMaskPalette
---

# HT_Get8BPPMaskPalette function


## -description

The <b>HT_Get8BPPMaskPalette</b> function returns a mask palette for an 8-bits-per-pixel device type.

## -parameters

### -param pPaletteEntry [in, out]

Pointer to the array of PALETTEENTRY structures (described in the Windows SDK documentation) to be filled in. GDI assumes that it points to valid memory space in which GDI can place the entire 8-bit-per-pixel halftone palette. 

For a driver that runs on Windows XP and later operating system versions, GDI checks <i>pPaletteEntry</i>[0] to determine how to return the composed CMY palette. If <i>pPaletteEntry</i>[0] is set to 'RGB0', the palette will be in one of the CMY_INVERTED modes and will have its indexes inverted. That is, index 0 in the palette is black, and index 255 is white. If <i>pPaletteEntry</i>[0] is not set to 'RGB0', the palette is a normal CMY palette, with index 0 being white and index 255 being black. See <a href="/windows-hardware/drivers/display/using-gdi-8-bit-per-pixel-cmy-mask-modes">Using GDI 8-Bit-Per-Pixel CMY Mask Modes</a> for new requirements and details on how to use this parameter.

Windows 2000 ignores any value the driver places in <i>pPaletteEntry</i>[0]. For this reason, if your driver is intended to run on Windows 2000 <i>and</i> on Windows XP or later versions, and your driver sets <i>pPaletteEntry</i>[0] to 'RGB0', the bitmaps your driver receives from Windows XP and later might have their colors inverted, relative to those received from Windows 2000. Therefore, such a driver must examine the palette before downloading a bitmap.

### -param Use8BPPMaskPal [in]

Indicates which type of palette should be returned. When <i>Use8BPPMaskPal</i> is <b>TRUE</b>, <b>HT_Get8BPPMaskPalette</b> sets the <i>pPaletteEntry</i> parameter with the address of a CMY palette (an array of PALETTEENTRY structures) that is described by the bitmask specified in <i>CMYMask</i>. When <i>Use8BPPMaskPal</i> is <b>FALSE</b>, the function sets <i>pPaletteEntry</i> with the address of a standard RGB 8-bit-per-pixel halftone palette.

### -param CMYMask [in]

Specifies information about the array of PALETTEENTRY structures pointed to by <i>pPaletteEntry</i>. This parameter can have one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
Gray scale with 256 levels

</td>
</tr>
<tr>
<td>
1

</td>
<td>
Five levels each of cyan, magenta, and yellow (each ranging from 0 to 4), for a total of 125 colors

</td>
</tr>
<tr>
<td>
2

</td>
<td>
Six levels each of cyan, magenta, and yellow (each ranging from 0 to 5), for a total of 216 colors

</td>
</tr>
<tr>
<td>
3 to 255

</td>
<td>
A bitmask that specifies that maximum number of levels of cyan, magenta, and yellow, respectively.

</td>
</tr>
</table>
 

Drivers running on Windows 2000 should be restricted to 8-bits-per-pixel monochrome. That is, the value of <i>CMYMask</i> used should be 0. 

For Windows XP and later operating system versions, and for all values of <i>CMYMask</i>, the value in <i>pPaletteEntry</i>[0] determines whether the palette that follows <i>pPaletteEntry</i>[0] is a normal CMY palette, or one of the CMY_INVERTED mode palettes. For more information, see the description of the <i>pPaletteEntry</i> parameter.

For values of <i>CMYMask</i> from 3 to 255, inclusive, the value is a bitmask in which groups of bits have the following meanings:

<ul>
<li>
The three highest bits (bits 7,6,5) specify the number of levels of cyan. At most, seven levels of cyan (levels 1 to 7) are possible.

</li>
<li>
The middle three bits (bits 4,3,2) specify the number of levels of magenta. At most, seven levels of magenta (levels 1 to 7) are possible.

</li>
<li>
The two lowest bits (bits 1,0) specify the number of levels of yellow. At most, three levels of yellow (levels 1 to 3) are possible.

</li>
</ul>
For values of <i>CMYMask</i> ranging from 3 to 255, any bitmask combination in which the cyan, magenta, or yellow level bits are zero is invalid. In such cases, <b>HT_Get8BPPMaskPalette</b> returns a palette count of zero. See <a href="/windows-hardware/drivers/display/using-gdi-8-bit-per-pixel-cmy-mask-modes">Using GDI 8-Bit-Per-Pixel CMY Mask Modes</a> for more information.

### -param RedGamma [in]

If <i>Use8BPPMaskPal</i> is <b>TRUE</b>, the value of this parameter is  not used. In that case, gamma values will be specified in the <b>ciDevice</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a> structure. 

If <i>Use8BPPMaskPal</i> is <b>FALSE</b>, the value of this parameter specifies the red gamma value, out of the red, green and blue gamma values that GDI is to use to gamma-correct the palette. The USHORT value is interpreted as a real number whose four least-significant digits are to the right of the decimal point. For example, a gamma value of 10000 represents the real number 1.0000, and 12345 represents 1.2345. The minimum gamma value allowed is 0.0000, and the maximum allowable value is 6.5535.

### -param GreenGamma [in]

If <i>Use8BPPMaskPal</i> is <b>TRUE</b>, the value of this parameter is  not used. In that case, gamma values will be specified in the <b>ciDevice</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a> structure. 

If <i>Use8BPPMaskPal</i> is <b>FALSE</b>, the value of this parameter specifies the green gamma value, out of the red, green and blue gamma values that GDI is to use to gamma-correct the palette. The USHORT value is interpreted as a real number whose four least-significant digits are to the right of the decimal point. For example, a gamma value of 10000 represents the real number 1.0000, and 12345 represents 1.2345. The minimum gamma value allowed is 0.0000, and the maximum allowable value is 6.5535.

### -param BlueGamma [in]

If <i>Use8BPPMaskPal</i> is <b>TRUE</b>, the value of this parameter is  not used. In that case, gamma values will be specified in the <b>ciDevice</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a> structure. 

If <i>Use8BPPMaskPal</i> is <b>FALSE</b>, the value of this parameter specifies the blue gamma value, out of the red, green and blue gamma values that GDI is to use to gamma-correct the palette. The USHORT value is interpreted as a real number whose four least-significant digits are to the right of the decimal point. For example, a gamma value of 10000 represents the real number 1.0000, and 12345 represents 1.2345. The minimum gamma value allowed is 0.0000, and the maximum allowable value is 6.5535.

## -returns

If <i>pPaletteEntry</i> is not <b>NULL</b>, <b>HT_Get8BPPMaskPalette</b> returns the number of PALETTEENTRY structures that GDI filled out in the array to which <i>pPaletteEntry</i> points. If <i>pPaletteEntry</i> is <b>NULL</b>, the value returned is the total count of PALETTEENTRY structures required to store the halftone palette.

If an illegal value of the <i>CMYMask</i> parameter is used in the call to this function, <b>HT_Get8BPPMaskPalette</b> returns a value of zero.

## -remarks

The PALETTEENTRY structure is documented in the Windows SDK documentation.

Calling <b>HT_Get8BPPMaskPalette</b> with <i>Use8BPPMaskPal</i> set <b>FALSE</b> is equivalent to calling <a href="/windows/desktop/api/winddi/nf-winddi-ht_get8bppformatpalette">HT_Get8BPPFormatPalette</a>.

See <a href="/windows-hardware/drivers/display/using-gdi-8-bit-per-pixel-cmy-mask-modes">Using GDI 8-Bit-Per-Pixel CMY Mask Modes</a> for more information about this function and how its parameters are used.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-ht_get8bppformatpalette">HT_Get8BPPFormatPalette</a>