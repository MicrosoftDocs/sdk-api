---
UID: NS:wingdi.tagCOLORADJUSTMENT
title: COLORADJUSTMENT (wingdi.h)
description: The COLORADJUSTMENT structure defines the color adjustment values used by the StretchBlt and StretchDIBits functions when the stretch mode is HALFTONE. You can set the color adjustment values by calling the SetColorAdjustment function.
helpviewer_keywords: ["*LPCOLORADJUSTMENT","*PCOLORADJUSTMENT","COLORADJUSTMENT","COLORADJUSTMENT structure [Windows GDI]","PCOLORADJUSTMENT","PCOLORADJUSTMENT structure pointer [Windows GDI]","_win32_COLORADJUSTMENT_str","gdi.coloradjustment","wingdi/COLORADJUSTMENT","wingdi/PCOLORADJUSTMENT"]
old-location: gdi\coloradjustment.htm
tech.root: gdi
ms.assetid: 9a080f60-0bce-46b6-b8a8-f534ff83a0a8
ms.date: 12/05/2018
ms.keywords: '*LPCOLORADJUSTMENT, *PCOLORADJUSTMENT, COLORADJUSTMENT, COLORADJUSTMENT structure [Windows GDI], PCOLORADJUSTMENT, PCOLORADJUSTMENT structure pointer [Windows GDI], _win32_COLORADJUSTMENT_str, gdi.coloradjustment, wingdi/COLORADJUSTMENT, wingdi/PCOLORADJUSTMENT'
req.header: wingdi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COLORADJUSTMENT, *PCOLORADJUSTMENT, *LPCOLORADJUSTMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOLORADJUSTMENT
 - wingdi/tagCOLORADJUSTMENT
 - PCOLORADJUSTMENT
 - wingdi/PCOLORADJUSTMENT
 - COLORADJUSTMENT
 - wingdi/COLORADJUSTMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - COLORADJUSTMENT
---

# COLORADJUSTMENT structure


## -description

The <b>COLORADJUSTMENT</b> structure defines the color adjustment values used by the <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a> functions when the stretch mode is HALFTONE. You can set the color adjustment values by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-setcoloradjustment">SetColorAdjustment</a> function.

## -struct-fields

### -field caSize

The size, in bytes, of the structure.

### -field caFlags

Specifies how the output image should be prepared. This member may be set to <b>NULL</b> or any combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CA_NEGATIVE</td>
<td>Specifies that the negative of the original image should be displayed.</td>
</tr>
<tr>
<td>CA_LOG_FILTER</td>
<td>Specifies that a logarithmic function should be applied to the final density of the output colors. This will increase the color contrast when the luminance is low.</td>
</tr>
</table>

### -field caIlluminantIndex

The type of standard light source under which the image is viewed. This member may be set to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>ILLUMINANT_DEVICE_DEFAULT</td>
<td>Device's default. Standard used by output devices.</td>
</tr>
<tr>
<td>ILLUMINANT_A</td>
<td>Tungsten lamp.</td>
</tr>
<tr>
<td>ILLUMINANT_B</td>
<td>Noon sunlight.</td>
</tr>
<tr>
<td>ILLUMINANT_C</td>
<td>NTSC daylight.</td>
</tr>
<tr>
<td>ILLUMINANT_D50</td>
<td>Normal print.</td>
</tr>
<tr>
<td>ILLUMINANT_D55</td>
<td>Bond paper print.</td>
</tr>
<tr>
<td>ILLUMINANT_D65</td>
<td>Standard daylight. Standard for CRTs and pictures.</td>
</tr>
<tr>
<td>ILLUMINANT_D75</td>
<td>Northern daylight.</td>
</tr>
<tr>
<td>ILLUMINANT_F2</td>
<td>Cool white lamp.</td>
</tr>
<tr>
<td>ILLUMINANT_TUNGSTEN</td>
<td>Same as ILLUMINANT_A.</td>
</tr>
<tr>
<td>ILLUMINANT_DAYLIGHT</td>
<td>Same as ILLUMINANT_C.</td>
</tr>
<tr>
<td>ILLUMINANT_FLUORESCENT</td>
<td>Same as ILLUMINANT_F2.</td>
</tr>
<tr>
<td>ILLUMINANT_NTSC</td>
<td>Same as ILLUMINANT_C.</td>
</tr>
</table>

### -field caRedGamma

Specifies the <i>n</i><sup>th</sup> power gamma-correction value for the red primary of the source colors. The value must be in the range from 2500 to 65,000. A value of 10,000 means no gamma correction.

### -field caGreenGamma

Specifies the <i>n</i><sup>th</sup> power gamma-correction value for the green primary of the source colors. The value must be in the range from 2500 to 65,000. A value of 10,000 means no gamma correction.

### -field caBlueGamma

Specifies the <i>n</i><sup>th</sup> power gamma-correction value for the blue primary of the source colors. The value must be in the range from 2500 to 65,000. A value of 10,000 means no gamma correction.

### -field caReferenceBlack

The black reference for the source colors. Any colors that are darker than this are treated as black. The value must be in the range from 0 to 4000.

### -field caReferenceWhite

The white reference for the source colors. Any colors that are lighter than this are treated as white. The value must be in the range from 6000 to 10,000.

### -field caContrast

The amount of contrast to be applied to the source object. The value must be in the range from -100 to 100. A value of 0 means no contrast adjustment.

### -field caBrightness

The amount of brightness to be applied to the source object. The value must be in the range from -100 to 100. A value of 0 means no brightness adjustment.

### -field caColorfulness

The amount of colorfulness to be applied to the source object. The value must be in the range from -100 to 100. A value of 0 means no colorfulness adjustment.

### -field caRedGreenTint

The amount of red or green tint adjustment to be applied to the source object. The value must be in the range from -100 to 100. Positive numbers adjust toward red and negative numbers adjust toward green. Zero means no tint adjustment.

## -see-also

<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcoloradjustment">GetColorAdjustment
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setcoloradjustment">SetColorAdjustment
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits
      </a>