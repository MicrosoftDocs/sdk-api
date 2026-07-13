---
UID: NS:wingdi.tagLOGCOLORSPACEA
title: LOGCOLORSPACEA (wingdi.h)
description: The LOGCOLORSPACE structure contains information that defines a logical color space. (ANSI)
helpviewer_keywords: ["*LPLOGCOLORSPACEA","LOGCOLORSPACE","LOGCOLORSPACE structure [Windows Color System]","LOGCOLORSPACEA","LPLOGCOLORSPACE","LPLOGCOLORSPACE structure pointer [Windows Color System]","_color_LOGCOLORSPACE_str","wcs.logcolorspace","wingdi/LOGCOLORSPACE","wingdi/LPLOGCOLORSPACE"]
old-location: wcs\logcolorspace.htm
tech.root: WCS
ms.assetid: b08aec07-6ac0-47be-8dc9-d604d94dedde
ms.date: 12/05/2018
ms.keywords: '*LPLOGCOLORSPACEA, LOGCOLORSPACE, LOGCOLORSPACE structure [Windows Color System], LOGCOLORSPACEA, LPLOGCOLORSPACE, LPLOGCOLORSPACE structure pointer [Windows Color System], _color_LOGCOLORSPACE_str, wcs.logcolorspace, wingdi/LOGCOLORSPACE, wingdi/LPLOGCOLORSPACE'
req.header: wingdi.h
req.include-header: 
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
req.typenames: LOGCOLORSPACEA, *LPLOGCOLORSPACEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLOGCOLORSPACEA
 - wingdi/tagLOGCOLORSPACEA
 - LPLOGCOLORSPACEA
 - wingdi/LPLOGCOLORSPACEA
 - LOGCOLORSPACEA
 - wingdi/LOGCOLORSPACEA
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
 - LOGCOLORSPACE
---

# LOGCOLORSPACEA structure


## -description

The <b>LOGCOLORSPACE</b> structure contains information that defines a logical [color space](/windows/win32/wcs/c#color-space).

## -struct-fields

### -field lcsSignature

Color space signature. At present, this member should always be set to LCS_SIGNATURE.

### -field lcsVersion

Version number; must be 0x400.

### -field lcsSize

Size of this structure, in bytes.

### -field lcsCSType

Color space type. The member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>LCS_CALIBRATED_RGB</td>
<td>Color values are calibrated RGB values. The values are translated using the endpoints specified by the <b>lcsEndpoints</b> member before being passed to the device.</td>
</tr>
<tr>
<td>LCS_sRGB</td>
<td>Color values are values are sRGB values.</td>
</tr>
<tr>
<td>LCS_WINDOWS_COLOR_SPACE</td>
<td>Color values are Windows default color space color values.</td>
</tr>
</table>
 

If LCS_CALIBRATED_RGB is not specified, the <b>lcsEndpoints</b> member is ignored.

### -field lcsIntent

The gamut mapping method. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Intent</th>
<th>ICC Name</th>
<th>Meaning</th>
</tr>
<tr>
<td>LCS_GM_ABS_<div> </div>COLORIMETRIC</td>
<td>Match</td>
<td>Absolute Colorimetric</td>
<td>Maintain the white point. Match the colors to their nearest color in the destination gamut.</td>
</tr>
<tr>
<td>LCS_GM_<div> </div>BUSINESS</td>
<td>Graphic</td>
<td>Saturation</td>
<td>Maintain saturation. Used for business charts and other situations in which undithered colors are required.</td>
</tr>
<tr>
<td>LCS_GM_<div> </div>GRAPHICS</td>
<td>Proof</td>
<td>Relative Colorimetric</td>
<td>Maintain colorimetric match. Used for graphic designs and named colors.</td>
</tr>
<tr>
<td>LCS_GM_<div> </div>IMAGES</td>
<td>Picture</td>
<td>Perceptual</td>
<td>Maintain contrast. Used for photographs and natural images.</td>
</tr>
</table>

### -field lcsEndpoints

Red, green, blue endpoints.

### -field lcsGammaRed

Scale of the red coordinate.

### -field lcsGammaGreen

Scale of the green coordinate.

### -field lcsGammaBlue

Scale of the blue coordinate.

### -field lcsFilename

A null-terminated string that names a color profile file. This member is typically set to zero, but may be used to set the color space to be exactly as specified by the color profile. This is useful for devices that input color values for a specific printer, or when using an installable image color matcher. If a color profile is specified, all other members of this structure should be set to reasonable values, even if the values are not completely accurate.

## -remarks

Like palettes, but unlike pens and brushes, a pointer must be passed when creating a LogColorSpace.

If the <b>lcsCSType</b> member is set to LCS_sRGB or LCS_WINDOWS_COLOR_SPACE, the other members of this structure are ignored, and WCS uses the sRGB color space. The <b>lcsEndpoints,</b><b>lcsGammaRed, lcsGammaGreen,</b> and <b>lcsGammaBlue</b> members are used to describe the logical color space. The <b>lcsEndpoints</b> member is a <b>CIEXYZTRIPLE</b> that contains the x, y, and z values of the color space's RGB endpoint.

The required DWORD bit format for the <b>lcsGammaRed</b>, <b>lcsGammaGreen</b>, and <b>lcsGammaBlue</b> is an 8.8 fixed point integer left-shifted by 8 bits. This means 8 integer bits are followed by 8 fraction bits. Taking the bit shift into account, the required format of the 32-bit DWORD is:

00000000nnnnnnnnffffffff00000000

Whenever the <b>lcsFilename</b> member contains a file name and the <b>lcsCSType</b> member is set to LCS_CALIBRATED_RGB, WCS ignores the other members of this structure. It uses the color space in the file as the color space to which this <b>LOGCOLORSPACE</b> structure refers.

The relation between tri-stimulus values X,Y,Z and chromaticity values x,y,z is as follows:

x = X/(X+Y+Z)

y = Y/(X+Y+Z)

z = Z/(X+Y+Z)

If the lcsCSType member is set to LCS_sRGB or LCS_WINDOWS_COLOR_SPACE, the other members of this structure are ignored, and ICM uses the sRGB color space. Applications should still initialize the rest of the structure since CreateProfileFromLogColorSpace ignores lcsCSType member and uses lcsEndpoints, lcsGammaRed, lcsGammaGreen, lcsGammaBlue members to create a profile, which may not be initialized in case of LCS_sRGB or LCS_WINDOWS_COLOR_SPACE color spaces.





> [!NOTE]
> The wingdi.h header defines LOGCOLORSPACE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv4header">BITMAPV4HEADER</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header">BITMAPV5HEADER</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-cmyk">CMYK</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
