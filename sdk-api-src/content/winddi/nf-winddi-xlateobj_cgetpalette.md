---
UID: NF:winddi.XLATEOBJ_cGetPalette
title: XLATEOBJ_cGetPalette function (winddi.h)
description: The XLATEOBJ_cGetPalette function retrieves RGB colors or the bitfields format from the specified palette.
helpviewer_keywords: ["XLATEOBJ_cGetPalette","XLATEOBJ_cGetPalette function [Display Devices]","display.xlateobj_cgetpalette","gdifncs_739e9529-598b-4489-85ff-0057e244617e.xml","winddi/XLATEOBJ_cGetPalette"]
old-location: display\xlateobj_cgetpalette.htm
tech.root: display
ms.assetid: eec6a5ec-398a-484f-b70f-e6baaedc6abd
ms.date: 12/05/2018
ms.keywords: XLATEOBJ_cGetPalette, XLATEOBJ_cGetPalette function [Display Devices], display.xlateobj_cgetpalette, gdifncs_739e9529-598b-4489-85ff-0057e244617e.xml, winddi/XLATEOBJ_cGetPalette
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
 - XLATEOBJ_cGetPalette
 - winddi/XLATEOBJ_cGetPalette
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
 - XLATEOBJ_cGetPalette
---

# XLATEOBJ_cGetPalette function


## -description

The <b>XLATEOBJ_cGetPalette</b> function retrieves RGB colors or the bitfields format from the specified palette.

## -parameters

### -param pxlo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure from which GDI retrieves the requested information.

### -param iPal [in]

Identifies the palette information to be written. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
XO_DESTBITFIELDS

</td>
<td>
GDI retrieves the bitfields format of the destination palette.

</td>
</tr>
<tr>
<td>
XO_DESTPALETTE

</td>
<td>
GDI retrieves RGB colors from the destination palette.

</td>
</tr>
<tr>
<td>
XO_SRCBITFIELDS

</td>
<td>
GDI retrieves the bitfields format of the source palette.

</td>
</tr>
<tr>
<td>
XO_SRCPALETTE

</td>
<td>
GDI retrieves RGB colors from the source palette.

</td>
</tr>
</table>

### -param cPal

Specifies the number of entries in the buffer pointed to by <i>pPal</i>. This can be smaller than the total size of the palette.

### -param pPal

Pointer to a buffer in which GDI writes the requested palette information. If <i>iPal</i> is XO_SRCPALETTE or XO_DESTPALETTE and the respective palette type is PAL_INDEXED, each entry is a 24-bit RGB value.

If <i>iPal</i> is XO_SRCBITFIELDS or XO_DESTBITFIELDS and the respective palette type is PAL_BITFIELDS, PAL_RGB, or PAL_BGR, <i>pPal</i> points to three ULONG masks that represent the red, green, and blue color masks.

## -returns

<b>XLATEOBJ_cGetPalette</b> returns the number of entries written if <i>pPal</i> is not null. A value of zero is returned if the XLATEOBJ is null or its palette is invalid. <b>XLATEOBJ_cGetPalette</b> will also return zero if the data pointed to by <i>pxlo</i> is not consistent with the value in <i>iPal</i>. For example, if the data pointed to is a bitfield, but <i>iPal</i> is set to either XO_SRCPALETTE or XO_DESTPALETTE, <b>XLATEOBJ_cGetPalette</b> will return zero. Similarly, if the data pointed to by <i>pxlo</i> is a palette, but <i>iPal</i> is set to either XO_SRCBITFIELDS or XO_DESTBITFIELDS, <b>XLATEOBJ_cGetPalette</b> also returns zero.

## -remarks

The driver must have information about the palette to perform some methods of color blending.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>