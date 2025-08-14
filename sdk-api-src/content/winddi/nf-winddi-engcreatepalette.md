---
UID: NF:winddi.EngCreatePalette
title: EngCreatePalette function (winddi.h)
description: The EngCreatePalette function sends a request to GDI to create an RGB palette.
helpviewer_keywords: ["EngCreatePalette","EngCreatePalette function [Display Devices]","display.engcreatepalette","gdifncs_53382d1c-5765-48ee-904b-52dc46338d38.xml","winddi/EngCreatePalette"]
old-location: display\engcreatepalette.htm
tech.root: display
ms.assetid: 99b27e11-5a5f-4fa7-9cd0-422d24425fa1
ms.date: 12/05/2018
ms.keywords: EngCreatePalette, EngCreatePalette function [Display Devices], display.engcreatepalette, gdifncs_53382d1c-5765-48ee-904b-52dc46338d38.xml, winddi/EngCreatePalette
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
 - EngCreatePalette
 - winddi/EngCreatePalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngCreatePalette
---

# EngCreatePalette function


## -description

The <b>EngCreatePalette</b> function sends a request to GDI to create an RGB palette.

## -parameters

### -param iMode [in]

Specifies how the palette will be defined. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
PAL_BITFIELDS

</td>
<td>
The palette is defined by the <i>flRed</i>, <i>flGreen</i>, and <i>flBlue</i> parameters.

</td>
</tr>
<tr>
<td>
PAL_BGR

</td>
<td>
The device accepts RGB colors directly, with B (blue) as the least significant byte.

</td>
</tr>
<tr>
<td>
PAL_CMYK

</td>
<td>
The device accepts CMYK colors directly, with C (cyan) as the least significant byte.

</td>
</tr>
<tr>
<td>
PAL_INDEXED

</td>
<td>
An array of RGB colors is provided with <i>cColors</i> and <i>pulColors</i>.

</td>
</tr>
<tr>
<td>
PAL_RGB

</td>
<td>
The device accepts RGB colors directly, with R (red) as the least significant byte.

</td>
</tr>
</table>

### -param cColors [in]

If the <i>iMode</i> parameter is PAL_INDEXED, <i>cColors</i> specifies the number of colors provided in the array pointed to by <i>pulColors</i>. Otherwise, this parameter should be zero.

### -param pulColors [in]

Pointer to the beginning of an array of ULONG values if <i>iMode</i> is PAL_INDEXED. The low-order 3 bytes of each ULONG define the RGB colors in the palette.

### -param flRed [in]

If the <i>iMode</i> parameter is PAL_BITFIELDS, the <i>flRed</i>, <i>flGreen</i> and <i>flBlue</i> parameters are masks that show which bits correspond to red, green, and blue. Each mask must consist of contiguous bits and should not overlap other masks. All combinations of bitfields are supported by GDI.

### -param flGreen [in]

If the <i>iMode</i> parameter is PAL_BITFIELDS, the <i>flRed</i>, <i>flGreen</i> and <i>flBlue</i> parameters are masks that show which bits correspond to red, green, and blue. Each mask must consist of contiguous bits and should not overlap other masks. All combinations of bitfields are supported by GDI.

### -param flBlue [in]

If the <i>iMode</i> parameter is PAL_BITFIELDS, the <i>flRed</i>, <i>flGreen</i> and <i>flBlue</i> parameters are masks that show which bits correspond to red, green, and blue. Each mask must consist of contiguous bits and should not overlap other masks. All combinations of bitfields are supported by GDI.

## -returns

The return value is a handle to the new palette if the function is successful. Otherwise, it is zero, and an error code is logged.

## -remarks

The driver can associate the new palette with a device by returning a pointer to the palette in the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure.

A PAL_INDEXED palette associated with the device must have its first index entry set to black (red = 0, green = 0, blue = 0) and its last entry set to white (255, 255, 255). All other entries should be set so that entries whose indexes are one's complements of each other have colors that contrast greatly. For example, if entry 0x9 of a 16 entry palette is set to pure green (0,255,0), entry 0x6 (=~0x9) should be set to a color that contrasts well with green, such as dark purple (128,0,128). Setting entries in this way allows XOR raster operations to behave reasonably. You should delete the palette when you no longer need it by using <a href="/windows/win32/api/winddi/nf-winddi-engdeletepalette">EngDeletePalette</a>.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvsetpalette">DrvSetPalette</a>



<a href="/windows/win32/api/winddi/nf-winddi-engdeletepalette">EngDeletePalette</a>
