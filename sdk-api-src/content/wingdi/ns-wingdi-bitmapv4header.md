---
UID: NS:wingdi.BITMAPV4HEADER
title: BITMAPV4HEADER (wingdi.h)
description: The BITMAPV4HEADER structure is the bitmap information header file. It is an extended version of the BITMAPINFOHEADER structure.Applications can use the BITMAPV5HEADER structure for added functionality.
helpviewer_keywords: ["*LPBITMAPV4HEADER","*PBITMAPV4HEADER","BITMAPV4HEADER","BITMAPV4HEADER structure [Windows GDI]","PBITMAPV4HEADER","PBITMAPV4HEADER structure pointer [Windows GDI]","_win32_BITMAPV4HEADER_str","gdi.bitmapv4header","wingdi/BITMAPV4HEADER","wingdi/PBITMAPV4HEADER"]
old-location: gdi\bitmapv4header.htm
tech.root: gdi
ms.assetid: 17c50d55-1c95-4178-82ba-7f504aa63c83
ms.date: 12/05/2018
ms.keywords: '*LPBITMAPV4HEADER, *PBITMAPV4HEADER, BITMAPV4HEADER, BITMAPV4HEADER structure [Windows GDI], PBITMAPV4HEADER, PBITMAPV4HEADER structure pointer [Windows GDI], _win32_BITMAPV4HEADER_str, gdi.bitmapv4header, wingdi/BITMAPV4HEADER, wingdi/PBITMAPV4HEADER'
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
req.typenames: BITMAPV4HEADER, *LPBITMAPV4HEADER, *PBITMAPV4HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPBITMAPV4HEADER
 - wingdi/LPBITMAPV4HEADER
 - BITMAPV4HEADER
 - wingdi/BITMAPV4HEADER
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
 - BITMAPV4HEADER
---

# BITMAPV4HEADER structure


## -description

The <b>BITMAPV4HEADER</b> structure is the bitmap information header file. It is an extended version of the <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

Applications can use the 
        <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header">BITMAPV5HEADER</a> structure for added functionality.

## -struct-fields

### -field bV4Size

The number of bytes required by the structure. Applications should use this member to determine which bitmap information header structure is being used.

### -field bV4Width

The width of the bitmap, in pixels.

 If <b>bV4Compression</b> is BI_JPEG or BI_PNG, <b>bV4Width</b> specifies the width of the JPEG or PNG image in pixels.

### -field bV4Height

The height of the bitmap, in pixels. If <b>bV4Height</b> is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner. If <b>bV4Height</b> is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.

If <b>bV4Height</b> is negative, indicating a top-down DIB, <b>bV4Compression</b> must be either BI_RGB or BI_BITFIELDS. Top-down DIBs cannot be compressed.

 If <b>bV4Compression</b> is BI_JPEG or BI_PNG, <b>bV4Height</b> specifies the height of the JPEG or PNG image in pixels.

### -field bV4Planes

The number of planes for the target device. This value must be set to 1.

### -field bV4BitCount

The number of bits-per-pixel. The <b>bV4BitCount</b> member of the <b>BITMAPV4HEADER</b> structure determines the number of bits that define each pixel and the maximum number of colors in the bitmap. This member must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td> The number of bits-per-pixel is specified or is implied by the JPEG or PNG file format.</td>
</tr>
<tr>
<td>1</td>
<td>The bitmap is monochrome, and the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> contains two entries. Each bit in the bitmap array represents a pixel. If the bit is clear, the pixel is displayed with the color of the first entry in the <b>bmiColors</b> table; if the bit is set, the pixel has the color of the second entry in the table.</td>
</tr>
<tr>
<td>4</td>
<td>The bitmap has a maximum of 16 colors, and the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> contains up to 16 entries. Each pixel in the bitmap is represented by a 4-bit index into the color table. For example, if the first byte in the bitmap is 0x1F, the byte represents two pixels. The first pixel contains the color in the second table entry, and the second pixel contains the color in the sixteenth table entry.</td>
</tr>
<tr>
<td>8</td>
<td>The bitmap has a maximum of 256 colors, and the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> contains up to 256 entries. In this case, each byte in the array represents a single pixel.</td>
</tr>
<tr>
<td>16</td>
<td>The bitmap has a maximum of 2^16 colors. If the <b>bV4Compression</b> member of the <b>BITMAPV4HEADER</b> structure is BI_RGB, the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> is <b>NULL</b>. Each <b>WORD</b> in the bitmap array represents a single pixel. The relative intensities of red, green, and blue are represented with five bits for each color component. The value for blue is in the least significant five bits, followed by five bits each for green and red, respectively. The most significant bit is not used. The <b>bmiColors</b> color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the <b>bV4ClrUsed</b> member of the <b>BITMAPV4HEADER</b>.If the <b>bV4Compression</b> member of the <b>BITMAPV4HEADER</b> is BI_BITFIELDS, the <b>bmiColors</b> member contains three <b>DWORD</b> color masks that specify the red, green, and blue components of each pixel. Each <b>WORD</b> in the bitmap array represents a single pixel.

</td>
</tr>
<tr>
<td>24</td>
<td>The bitmap has a maximum of 2^24 colors, and the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> is <b>NULL</b>. Each 3-byte triplet in the bitmap array represents the relative intensities of blue, green, and red for a pixel. The <b>bmiColors</b> color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the <b>bV4ClrUsed</b> member of the <b>BITMAPV4HEADER</b>.</td>
</tr>
<tr>
<td>32</td>
<td>The bitmap has a maximum of 2^32 colors. If the <b>bV4Compression</b> member of the <b>BITMAPV4HEADER</b> is BI_RGB, the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> is <b>NULL</b>. Each <b>DWORD</b> in the bitmap array represents the relative intensities of blue, green, and red for a pixel. The value for 
    blue is in the least significant 8 bits, followed by 8 bits each for green
    and red.  The high byte in each <b>DWORD</b> is not used. The <b>bmiColors</b> color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the <b>bV4ClrUsed</b> member of the <b>BITMAPV4HEADER</b>.If the <b>bV4Compression</b> member of the <b>BITMAPV4HEADER</b> is BI_BITFIELDS, the <b>bmiColors</b> member contains three <b>DWORD</b> color masks that specify the red, green, and blue components of each pixel. Each <b>DWORD</b> in the bitmap array represents a single pixel.

</td>
</tr>
</table>

### -field bV4V4Compression

The type of compression for a compressed bottom-up bitmap (top-down DIBs cannot be compressed). This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>BI_RGB</td>
<td>An uncompressed format.</td>
</tr>
<tr>
<td>BI_RLE8</td>
<td>A run-length encoded (RLE) format for bitmaps with 8 bpp. The compression format is a 2-byte format consisting of a count byte followed by a byte containing a color index. For more information, see <a href="/windows/desktop/gdi/bitmap-compression">Bitmap Compression</a>.</td>
</tr>
<tr>
<td>BI_RLE4</td>
<td>An RLE format for bitmaps with 4 bpp. The compression format is a 2-byte format consisting of a count byte followed by two word-length color indexes. For more information, see <a href="/windows/desktop/gdi/bitmap-compression">Bitmap Compression</a>.</td>
</tr>
<tr>
<td>BI_BITFIELDS</td>
<td>Specifies that the bitmap is not compressed. The members <b>bV4RedMask</b>, <b>bV4GreenMask</b>, and <b>bV4BlueMask</b> specify the red, green, and blue components for each pixel. This is valid when used with 16- and 32-bpp bitmaps.</td>
</tr>
<tr>
<td>BI_JPEG</td>
<td> Specifies that the image is compressed using the JPEG file interchange format. JPEG compression trades off compression against loss; it can achieve a compression ratio of 20:1 with little noticeable loss.</td>
</tr>
<tr>
<td>BI_PNG</td>
<td> Specifies that the image is compressed using the PNG file interchange format.</td>
</tr>
</table>

### -field bV4SizeImage

The size, in bytes, of the image. This may be set to zero for BI_RGB bitmaps.

 If <b>bV4Compression</b> is BI_JPEG or BI_PNG, <b>bV4SizeImage</b> is the size of the JPEG or PNG image buffer.

### -field bV4XPelsPerMeter

The horizontal resolution, in pixels-per-meter, of the target device for the bitmap. An application can use this value to select a bitmap from a resource group that best matches the characteristics of the current device.

### -field bV4YPelsPerMeter

The vertical resolution, in pixels-per-meter, of the target device for the bitmap.

### -field bV4ClrUsed

The number of color indexes in the color table that are actually used by the bitmap. If this value is zero, the bitmap uses the maximum number of colors corresponding to the value of the <b>bV4BitCount</b> member for the compression mode specified by <b>bV4Compression</b>.

If <b>bV4ClrUsed</b> is nonzero and the <b>bV4BitCount</b> member is less than 16, the <b>bV4ClrUsed</b> member specifies the actual number of colors the graphics engine or device driver accesses. If <b>bV4BitCount</b> is 16 or greater, the <b>bV4ClrUsed</b> member specifies the size of the color table used to optimize performance of the system color palettes. If <b>bV4BitCount</b> equals 16 or 32, the optimal color palette starts immediately following the <b>BITMAPV4HEADER</b>.

### -field bV4ClrImportant

The number of color indexes that are required for displaying the bitmap. If this value is zero, all colors are important.

### -field bV4RedMask

Color mask that specifies the red component of each pixel, valid only if <b>bV4Compression</b> is set to BI_BITFIELDS.

### -field bV4GreenMask

Color mask that specifies the green component of each pixel, valid only if <b>bV4Compression</b> is set to BI_BITFIELDS.

### -field bV4BlueMask

Color mask that specifies the blue component of each pixel, valid only if <b>bV4Compression</b> is set to BI_BITFIELDS.

### -field bV4AlphaMask

Color mask that specifies the alpha component of each pixel.

### -field bV4CSType

The color space of the DIB. The following table lists the value for <b>bV4CSType</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>LCS_CALIBRATED_RGB</td>
<td>This value indicates that endpoints and gamma values are given in the appropriate fields.</td>
</tr>
</table>
 

See the <a href="/windows/desktop/api/wingdi/ns-wingdi-logcolorspacea">LOGCOLORSPACE</a> structure for information that defines a logical color space.

### -field bV4Endpoints

A <a href="/windows/win32/api/wingdi/ns-wingdi-ciexyztriple">CIEXYZTRIPLE</a> structure that specifies the x, y, and z coordinates of the three colors that correspond to the red, green, and blue endpoints for the logical color space associated with the bitmap. This member is ignored unless the <b>bV4CSType</b> member specifies LCS_CALIBRATED_RGB.

<div class="alert"><b>Note</b>  A <i>color space</i> is a model for representing color numerically in terms of three or more coordinates. For example, the RGB color space represents colors in terms of the red, green, and blue coordinates.</div>
<div> </div>

### -field bV4GammaRed

Tone response curve for red. This member is ignored unless color values are calibrated RGB values and <b>bV4CSType</b> is set to LCS_CALIBRATED_RGB. Specify in unsigned fixed 16.16 format. The upper 16 bits are the unsigned integer value. The lower 16 bits are the fractional part.

### -field bV4GammaGreen

Tone response curve for green. Used if <b>bV4CSType</b> is set to LCS_CALIBRATED_RGB. Specify in unsigned fixed 16.16 format. The upper 16 bits are the unsigned integer value. The lower 16 bits are the fractional part.

### -field bV4GammaBlue

Tone response curve for blue. Used if <b>bV4CSType</b> is set to LCS_CALIBRATED_RGB. Specify in unsigned fixed 16.16 format. The upper 16 bits are the unsigned integer value. The lower 16 bits are the fractional part.

## -remarks

The <b>BITMAPV4HEADER</b> structure is extended to allow a JPEG or PNG image to be passed as the source image to <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header">BITMAPV5HEADER</a>



<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-ciexyztriple">CIEXYZTRIPLE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logcolorspacea">LOGCOLORSPACE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>

