---
UID: NS:winddi._GDIINFO
title: GDIINFO (winddi.h)
description: The GDIINFO structure describes the graphics capabilities of a given device.
helpviewer_keywords: ["*PGDIINFO","GDIINFO","GDIINFO structure [Display Devices]","PGDIINFO","PGDIINFO structure pointer [Display Devices]","display.gdiinfo","grstrcts_181c0d6e-5908-4505-8093-956eefc87c85.xml","winddi/GDIINFO","winddi/PGDIINFO"]
old-location: display\gdiinfo.htm
tech.root: display
ms.assetid: f75f599f-43ea-4da6-a6e3-6591cf6d69f1
ms.date: 12/05/2018
ms.keywords: '*PGDIINFO, GDIINFO, GDIINFO structure [Display Devices], PGDIINFO, PGDIINFO structure pointer [Display Devices], display.gdiinfo, grstrcts_181c0d6e-5908-4505-8093-956eefc87c85.xml, winddi/GDIINFO, winddi/PGDIINFO'
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GDIINFO, *PGDIINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GDIINFO
 - winddi/_GDIINFO
 - PGDIINFO
 - winddi/PGDIINFO
 - GDIINFO
 - winddi/GDIINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - GDIINFO
---

# GDIINFO structure


## -description

The GDIINFO structure describes the graphics capabilities of a given device.

## -struct-fields

### -field ulVersion

Specifies the driver version number. The byte ordering of <b>ulVersion</b> has the following form.

<img alt="Figure showing the ulVersion member specifying the driver version number" src="images/ver_nmbr.png"/>

The high-order 16 bits must be set to zero. Bits 8 through 15 specify the version number of the Microsoft operating system for which the driver is designed. The high-order 4 bits of this range specify the major number of the version, the low-order 4 bits contain the minor number of the version. The low-order 8 bits of <b>ulVersion</b> specify the version number of the display driver; this value should be incremented for each release of the display driver binary file.

The Display program in Control Panel indicates the version number contained in <b>ulVersion</b>, along with other driver-specific information.

### -field ulTechnology

Specifies the device technology. This member can be one of the values listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DT_CHARSTREAM

</td>
<td>
Device fonts only

</td>
</tr>
<tr>
<td>
DT_PLOTTER

</td>
<td>
Vector plotter

</td>
</tr>
<tr>
<td>
DT_RASCAMERA

</td>
<td>
Raster camera

</td>
</tr>
<tr>
<td>
DT_RASDISPLAY

</td>
<td>
Raster display

</td>
</tr>
<tr>
<td>
DT_RASPRINTER

</td>
<td>
Raster printer

</td>
</tr>
</table>

### -field ulHorzSize

Specifies the width of the physical surface. A positive value indicates that the width is in units of millimeters, while a negative value denotes that the width is in units of micrometers.

### -field ulVertSize

Specifies the height of the physical surface. A positive value indicates that the height is in units of millimeters, while a negative value denotes that the height is in units of micrometers.

### -field ulHorzRes

Specifies the width in pixels of the physical surface (display devices), or of the printable surface (printers). 

See also <b>ulDesktopHorzRes</b>.

### -field ulVertRes

Specifies the height in pixels of the physical surface (display devices), or of the printable surface (printers).

### -field cBitsPixel

Specifies the number of adjacent bits in each color plane. The total number of bits per pixel is the product of <b>cBitsPixel</b> and <b>cPlanes</b>.

### -field cPlanes

Specifies the number of color planes.

### -field ulNumColors

For palettized devices, <b>ulNumColors</b> specifies the number of entries in the default color palette. For nonpalettized devices (which do not include printers), <b>ulNumColors</b> is set to -1.

### -field flRaster

Is reserved and must be left set to zero.

### -field ulLogPixelsX

Specifies the width resolution of the device in logical pixels per inch.

For printers, this member should be set to the printer's resolution in dpi.

For displays, this member must be set to 96.

### -field ulLogPixelsY

Specifies the height resolution of the device in logical pixels per inch.

For printers, this member should be set to the printer's resolution in dpi.

For displays, this member must be set to 96.

### -field flTextCaps

Specifies a flag describing Windows 3.1 text capabilities. If the driver TC_SCROLLBLT flag is in this member, it indicates that the console should perform text scrolling by redrawing the entire screen, using the driver-supplied <a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a> function rather than the <a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a> or <a href="/windows/desktop/api/winddi/nf-winddi-drvcopybits">DrvCopyBits</a> functions. The driver should set this flag if screen-to-screen bit-block transfers are slow. If this flag is not set, the driver is implicitly requesting that the console perform text scrolls through <i>DrvBitBlt</i><b>/</b><i>DrvCopyBits</i>.

### -field ulDACRed

### -field ulDACGreen

### -field ulDACBlue

Specifies the display number of DAC bits for the specified color.

### -field ulAspectX

Specifies the relative width of a device pixel, in the range of one to 1000.

### -field ulAspectY

Specifies the relative height of a device pixel, in the range of one to 1000.

### -field ulAspectXY

Specifies the square root of the sum of the squares of <b>ulAspectX</b> and <b>ulAspectY</b>.

### -field xStyleStep

Specifies the numerator of style advance for x-major lines, <i>dx</i>. For additional information, refer to the following <b>Remarks</b> section and <a href="/windows-hardware/drivers/display/styled-cosmetic-lines">Styled Cosmetic Lines</a>.

### -field yStyleStep

Specifies the numerator of style advance for y-major lines, <i>dy</i>. For additional information, refer to the following <b>Remarks</b> section and <a href="/windows-hardware/drivers/display/styled-cosmetic-lines">Styled Cosmetic Lines</a>.

### -field denStyleStep

Specifies the denominator of style advance, D. For additional information, refer to the following <b>Remarks</b> section and <a href="/windows-hardware/drivers/display/styled-cosmetic-lines">Styled Cosmetic Lines</a>.

### -field ptlPhysOffset

Specifies a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that contains the size, in pixels, of the unwritable margin of a surface.

### -field szlPhysSize

Specifies a SIZEL structure that contains the size, in pixels, of the entire surface, including unwritable margins. A SIZEL structure is identical to a <a href="/windows/desktop/api/windef/ns-windef-size">SIZE</a> structure.

### -field ulNumPalReg

Specifies the number of palette registers for an indexed device.

### -field ciDevice

Is a <a href="/windows/desktop/api/winddi/ns-winddi-colorinfo">COLORINFO</a> structure that defines the device's colors in CIE coordinate space.

### -field ulDevicePelsDPI

For printers, specifies the number of pixels (or dots, or nozzles) per inch if the pixels are laid out side by side without overlapping or space between. For example, if the size of a pixel is 0.001 inch, this value is equal to one-divided-by 0.001. If the member is zero, GDI halftoning calculates this number based on the assumption that all pixels are connected with no overlapping. 

Because the physical dot size for most printers is larger than the measured dot size, GDI uses this value to approximate how many physical dots can be placed, based on the cell size (pattern size). A log regression is then performed to determine what is most linear; that is, where the dots should be placed for the best coverage to optimize the overlapped device pixels coverage (dot gain).

For displays, this member should be set to zero.

### -field ulPrimaryOrder

Specifies the bit order of the device's primary colors or plane numbers for the halftone output. This member can be one of the values listed in the following table.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
PRIMARY_ORDER_ABC

</td>
<td>
Device output order is RGB or CMY. Red or cyan is in the least significant bits; blue or yellow is in the most significant bits.

</td>
</tr>
<tr>
<td>
PRIMARY_ORDER_ACB

</td>
<td>
Device output order is RBG or CYM. Red or cyan is in the least significant bits; green or magenta is in the most significant bits.

</td>
</tr>
<tr>
<td>
PRIMARY_ORDER_BAC

</td>
<td>
Device output order is GRB or MCY. Green or magenta is in the least significant bits; blue or yellow is in the most significant bits.

</td>
</tr>
<tr>
<td>
PRIMARY_ORDER_BCA

</td>
<td>
Device output order is GBR or MYC. Green or magenta is in the least significant bits; red or cyan is in the most significant bits.

</td>
</tr>
<tr>
<td>
PRIMARY_ORDER_CBA

</td>
<td>
Device output order is BGR or YMC. Blue or yellow is in the least significant bits; red or cyan is in the most significant bits.

</td>
</tr>
<tr>
<td>
PRIMARY_ORDER_CAB

</td>
<td>
Device output order is BRG or YCM. Blue or yellow is in the least significant bits; green or magenta is in the most significant bits.

</td>
</tr>
</table>

### -field ulHTPatternSize

Specifies the size of the halftone pattern. The values ending with <i>A</i>x<i>B</i>_M are variations of the <i>A</i>x<i>B</i> patterns. In other words, SIZE_<i>A</i>x<i>B</i> and SIZE_<i>A</i>x<i>B</i>_M differ by which pixels are lit in an A x B pattern. This member can be one of the following values:


<dl>
<dt>HT_PATSIZE_2x2</dt>
<dt>HT_PATSIZE_2x2_M</dt>
<dt>HT_PATSIZE_4x4</dt>
<dt>HT_PATSIZE_4x4_M</dt>
<dt>HT_PATSIZE_6x6</dt>
<dt>HT_PATSIZE_6x6_M</dt>
<dt>HT_PATSIZE_8x8</dt>
<dt>HT_PATSIZE_8x8_M</dt>
<dt>HT_PATSIZE_10x10</dt>
<dt>HT_PATSIZE_10x10_M</dt>
<dt>HT_PATSIZE_12x12</dt>
<dt>HT_PATSIZE_12x12_M</dt>
<dt>HT_PATSIZE_14x14</dt>
<dt>HT_PATSIZE_14x14_M</dt>
<dt>HT_PATSIZE_16x16</dt>
<dt>HT_PATSIZE_16x16_M</dt>
<dt>HT_PATSIZE_SUPERCELL</dt>
<dt>HT_PATSIZE_SUPERCELL_M</dt>
<dt>HT_PATSIZE_USER</dt>
<dt>HT_PATSIZE_MAX_INDEX</dt>
<dt>HT_PATSIZE_DEFAULT</dt>
</dl>

### -field ulHTOutputFormat

Specifies the preferred output format for halftone. HT_FORMAT_4BPP uses only 8 full intensity colors while HT_FORMATP_IRGB uses all the 16 colors including the half-intensity colors. It is assumed that a 5 x 5 x 5 format (5 bits per color) is used for HT_FORMAT_16BPP. This member can be one of the following values:


<dl>
<dt>HT_FORMAT_1BPP</dt>
<dt>HT_FORMAT_4BPP</dt>
<dt>HT_FORMAT_4BPP_IRGB</dt>
<dt>HT_FORMAT_8BPP</dt>
<dt>HT_FORMAT_16BPP</dt>
<dt>HT_FORMAT_24BPP</dt>
<dt>HT_FORMAT_32BPP</dt>
</dl>

### -field flHTFlags

Specifies a combination of flags describing the device. These flags are needed for halftoning. This member can be a combination of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
HT_FLAG_8BPP_CMY332_MASK

</td>
<td>
Flag used to clear the upper eight bits of <b>flHTFlags</b> (bits 24 to 31). The <b>MAKE_CMY332_MASK</b> macro can then be used to set these bits with 8-bit-per-pixel CMY mode ink level information. See <a href="/windows-hardware/drivers/display/using-gdi-8-bit-per-pixel-cmy-mask-modes">Using GDI 8-Bit-Per-Pixel CMY Mask Modes</a> for more information.

</td>
</tr>
<tr>
<td>
HT_FLAG_ADDITIVE_PRIMS

</td>
<td>
Device primaries are additive.

</td>
</tr>
<tr>
<td>
HT_FLAG_DO_DEVCLR_XFORM

</td>
<td>
Requests GDI to perform generic color correction.

</td>
</tr>
<tr>
<td>
HT_FLAG_HAS_BLACK_DYE

</td>
<td>
Device has separate black dye.

</td>
</tr>
<tr>
<td>

<dl>
<dt>HT_FLAG_HIGH_INK_ABSORPTION</dt>
<dt>HT_FLAG_HIGHER_INK_ABSORPTION</dt>
<dt>HT_FLAG_HIGHEST_INK_ABSORPTION</dt>
</dl>


</td>
<td>
Paper in device absorbs more than normal amount of ink, so GDI should render less ink to paper. These flags indicate the relative amount of ink absorption, with HT_FLAG_HIGHER_INK_ABSORPTION denoting more absorption than HT_FLAG_HIGH_INK_ABSORPTION, but less than HT_FLAG_HIGHEST_INK_ABSORPTION. 

</td>
</tr>
<tr>
<td>

<dl>
<dt>HT_FLAG_INK_ABSORPTION_IDX0</dt>
<dt>HT_FLAG_INK_ABSORPTION_IDX1</dt>
<dt>HT_FLAG_INK_ABSORPTION_IDX2</dt>
<dt>HT_FLAG_INK_ABSORPTION_IDX3</dt>
</dl>


</td>
<td>
Flags used to define HT_FLAG_HIGH/HIGHER/HIGHEST_INK_ABSORPTION and HT_FLAG_LOW/LOWER/LOWEST_INK_ABSORPTION.

</td>
</tr>
<tr>
<td>
HT_FLAG_INK_HIGH_ABSORPTION

</td>
<td>
Flag used to define HT_FLAG_HIGH/HIGHER/HIGHEST_INK_ABSORPTION.

</td>
</tr>
<tr>
<td>
HT_FLAG_INVERT_8BPP_BITMASK_IDX

</td>
<td>
GDI halftone should render 8-bit-per-pixel ask mode surface bitmap using a CMY_INVERTED mode palette. See <a href="/windows-hardware/drivers/display/using-gdi-8-bit-per-pixel-cmy-mask-modes">Using GDI 8-Bit-Per-Pixel CMY Mask Modes</a> for CMY_INVERTED mode palette description and requirements.

</td>
</tr>
<tr>
<td>

<dl>
<dt>HT_FLAG_LOW_INK_ABSORPTION</dt>
<dt>HT_FLAG_LOWER_INK_ABSORPTION</dt>
<dt>HT_FLAG_LOWEST_INK_ABSORPTION</dt>
</dl>


</td>
<td>
Paper in device absorbs less than normal amount of ink, so GDI should render more ink to paper. These flags indicate the relative amount of ink absorption, with HT_FLAG_LOWER_INK_ABSORPTION denoting less absorption than HT_FLAG_LOW_INK_ABSORPTION, but more than HT_FLAG_LOWEST_INK_ABSORPTION. 

</td>
</tr>
<tr>
<td>
HT_FLAG_NORMAL_INK_ABSORPTION

</td>
<td>
Paper in device absorbs normal amount of ink.

</td>
</tr>
<tr>
<td>
HT_FLAG_OUTPUT_CMY

</td>
<td>
Device uses CMY primaries rather than RGB primaries. This flag value applies only to 1 bpp and 4 bpp destination surfaces.

</td>
</tr>
<tr>
<td>
HT_FLAG_PRINT_DRAFT_MODE

</td>
<td>
Disables GDI's antialiasing code.

</td>
</tr>
<tr>
<td>
HT_FLAG_SQUARE_DEVICE_PEL

</td>
<td>
Device pixel is square rather than round (displays only -- printers require rounded pixels).

</td>
</tr>
<tr>
<td>
HT_FLAG_USE_8BPP_BITMASK

</td>
<td>
Device uses monochrome printing.

</td>
</tr>
</table>

### -field ulVRefresh

The video refresh rate for the current display mode. This is the value returned by the miniport driver for the refresh rate for the current mode.

The Display program in Control Panel displays the refresh rate contained in the <b>ulVRefresh</b> member.

### -field ulBltAlignment

This member indicates the preferred x-alignment for bit block transfers to the device. A value of zero indicates that bit block transfers are accelerated; any other nonnegative number indicates that bit block transfers are not accelerated, and gives the preferred horizontal alignment as a pixel multiple.

This value is used by the system to determine the default alignment for window positions and is also used to set the initial full-drag default during setup. A value of zero indicates that full-drag should be on by default; any value other than zero indicates that full-drag should be off by default.

### -field ulPanningHorzRes

### -field ulPanningVertRes

Should be ignored by the driver and remain zero-initialized.

### -field xPanningAlignment

### -field yPanningAlignment

Should be ignored by the driver and remain zero-initialized.

### -field cxHTPat

### -field cyHTPat

Specify the width and height, respectively, in pixels, of the user-supplied halftone dither pattern. The value of <b>cxHTPat</b> must be in the range HT_USERPAT_CX_MIN to HT_USERPAT_CX_MAX, inclusive. The value of <b>cyHTPat</b> must be in the range HT_USERPAT_CY_MIN to HT_USERPAT_CY_MAX, inclusive. These constants are defined in <i>winddi.h</i>. See the following <b>Remarks</b> section for more information.

### -field pHTPatA

### -field pHTPatB

### -field pHTPatC

Point to the user-defined halftone dither patterns for primary colors A, B, and C, respectively, as defined by the PRIMARY_ORDER_XXX value in the <b>ulPrimaryOrder</b> member. Each dither pattern must be a valid two-dimensional byte array of size <b>cxHTPat</b> by <b>cyHTPat</b>. See the following <b>Remarks</b> section for more information.

### -field flShadeBlend

Specifies a set of flags that indicate the shading and blending capabilities of the device. Display drivers should ignore this member and should leave it set to zero. For printer drivers, the value that the driver places in this member is the value that GDI reports when an application calls <b>GetDeviceCaps</b>(hdc, SHADEBLENDCAPS). The <b>GetDeviceCaps</b> function is described in the Microsoft Window SDK documentation.

### -field ulPhysicalPixelCharacteristics

Specifies the way that color fragments are configured to form pixels on the display device. The color fragments on the display device can be arranged in RGB order, or in BGR order, completely independent of the RGB ordering in the <a href="/windows-hardware/drivers/">frame buffer</a>. The color fragments can be configured in horizontal stripes in which all of the fragments in one row are the same color. Alternatively, the color fragments can be configured in vertical stripes, in which all fragments in one column are the same color. Vertical striping is preferred, since it effectively provides three separate fragments in a row for each pixel, thereby giving greater horizontal subpixel resolution.  

The <b>ulPhysicalPixelCharacteristics</b> member must be set to one of the values shown in the following table:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
PPC_DEFAULT

</td>
<td>
Display device physical pixel information is unknown.

</td>
</tr>
<tr>
<td>
PPC_BGR_ORDER_HORIZONTAL_STRIPES

</td>
<td>
Physical color fragments on the display device are arranged, from top to bottom, in rows of blue, green, and red color fragments.

</td>
</tr>
<tr>
<td>
PPC_BGR_ORDER_VERTICAL_STRIPES

</td>
<td>
Physical color fragments on the display device are arranged, from left to right, in columns of blue, green, and red color fragments.

</td>
</tr>
<tr>
<td>
PPC_RGB_ORDER_HORIZONTAL_STRIPES

</td>
<td>
Physical color fragments on the display device are arranged, from top to bottom, in rows of red, green, and blue color fragments.

</td>
</tr>
<tr>
<td>
PPC_RGB_ORDER_VERTICAL_STRIPES

</td>
<td>
Physical color fragments on the display device are arranged, from left to right, in columns of red, green, and blue color fragments.

</td>
</tr>
<tr>
<td>
PPC_UNDEFINED

</td>
<td>
Display device physical pixel information is known but cannot be expressed as one of the given enumerations. The enumerations are currently applicable to an LCD-based monitor. The driver should set <b>ulPhysicalPixelCharacteristics</b> to PPC_UNDEFINED when either of the following conditions is met. (This list is not comprehensive, but covers the most common conditions.) 

<ul>
<li>
The driver has knowledge that the monitor is not an LCD device.

</li>
<li>
The device is an LCD device but the resolution of the frame buffer is different from the native resolution of the physical display requiring scaling. That is, scaling is required because there is no longer a one-to-one correspondence between frame buffer pixels and device pixels.

</li>
</ul>
</td>
</tr>
</table>

### -field ulPhysicalPixelGamma

Specifies the gamma of the display device. This member should be set to either the gamma of the physical pixel, scaled by a factor of 1000, or to one of the following values. For example, a gamma value of 2.2 would be represented as 2200.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
PPG_DEFAULT

</td>
<td>
The driver has no knowledge of the gamma for the device.

</td>
</tr>
<tr>
<td>
PPG_SRGB

</td>
<td>
The device uses an sRGB gamma.

</td>
</tr>
</table>

## -remarks

GDI zero-initializes this structure before calling the driver-supplied <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a> function.

The <b>xStyleStep</b>, <b>yStyleStep</b>, and <b>denStyleStep</b> members define how a cosmetic line style should advance as it draws each pixel of a cosmetic line. The amount advanced along the style for each pixel is defined as a fraction that depends on whether the line is x-styled or y-styled. If the line is x-styled, the style advances by the fractional amount <b>dx/D</b> for each pixel moved in the x direction. Otherwise the style advances by <b>dy/D</b> for each pixel moved in the y direction.

The dots in the predefined line style PS_DOT are each one unit long. If the driver defines <b>xStyleStep</b> as one and <b>denStyleStep</b> as 5, then a dotted horizontal line consists of 5-pixels-on followed by 5-pixels-off, repeated.

Each of these three numbers must be less than 65536, even though the caps members are LONG values. These style steps are defined by the driver to ensure that the dots and dashes in a line are a pleasing size on the output device. The horizontal and vertical steps can be different to correct for nontrivial aspect ratios. For example, on an EGA display, whose pixels are 33 percent higher than they are wide, you can set:


```
pdevcaps->xStyleStep   =  3;    // For an EGA
pdevcaps->yStyleStep   =  4;
pdevcaps->denStyleStep = 12;
```


In this case, horizontal dotted lines are 4-pixels-on, 4-pixels-off, because the style advances by 3/12 or 1/4 for each pixel. Vertical dotted lines are 3-pixels-on/3-pixels-off.

Styled lines look better if both the x and y style steps divide evenly into the style denominator, as they do in the preceding example. This gives dashes and dots that are always the same length.

GDI needs this information so that its bitmap functions can emulate exactly what the device does on its own surface. Applications can access this information to determine exactly which pixels will be turned on for styled lines. Refer also to <a href="/windows-hardware/drivers/display/styled-cosmetic-lines">Styled Cosmetic Lines</a>.

The halftone-related members, <b>cxHTPat</b>, <b>cyHTPat</b>, <b>pHTPatA</b>, <b>pHTPatB</b>, and <b>pHTPatC</b>, can be used in an OEM Unidrv rendering plug-in to define a custom halftone pattern consisting of either one or three colors. These members are checked only if the <b>ulHTPatternSize</b> member is set to HT_PATSIZE_USER. In this case an OEM can use these members to define a custom halftone pattern, based on data stored in a resource file or generated by an OEM customization module. The <b>cxHTPat</b> and <b>cyHTPat</b> members define the size of each of the three two-dimensional halftone pattern arrays. The <b>pHTPatA</b>, <b>pHTPatB</b>, and <b>pHTPatC</b> members point to the respective pattern arrays for each color. If only one pattern array is used, <b>pHTPatA</b>, <b>pHTPatB</b>, and<b> pHTPatC</b> point to it.

Each byte threshold at a particular location in a halftone dither pattern determines whether the pixel at the corresponding output plane location will be on or off. A zero threshold value at a particular location in the pattern array indicates that the corresponding pixel location is ignored (is black). Threshold values from 1 to 255 provide the dither pattern with 255 levels of gray; if the pixel value in the output plane is greater than or equal to the threshold value for that location, the pixel is turned on. A pixel value less than its corresponding threshold value causes its pixel to be turned off in the output plane. See <a href="/windows-hardware/drivers/print/customized-halftoning">Customized Halftoning</a> in <a href="/windows-hardware/drivers/print/customizing-microsoft-s-printer-drivers">Customizing Microsoft's Printer Drivers</a> for more information.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-ciechroma">CIECHROMA</a>



<a href="/windows/desktop/api/winddi/ns-winddi-colorinfo">COLORINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvcopybits">DrvCopyBits</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>