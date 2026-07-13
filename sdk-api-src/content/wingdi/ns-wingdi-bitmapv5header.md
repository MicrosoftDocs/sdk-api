---
UID: NS:wingdi.BITMAPV5HEADER
title: BITMAPV5HEADER (wingdi.h)
description: The BITMAPV5HEADER structure is the bitmap information header file. It is an extended version of the BITMAPINFOHEADER structure.
helpviewer_keywords: ["*LPBITMAPV5HEADER","*PBITMAPV5HEADER","BITMAPV5HEADER","BITMAPV5HEADER structure [Windows GDI]","PBITMAPV5HEADER","PBITMAPV5HEADER structure pointer [Windows GDI]","_win32_BITMAPV5HEADER_str","gdi.bitmapv5header","wingdi/BITMAPV5HEADER","wingdi/PBITMAPV5HEADER"]
old-location: gdi\bitmapv5header.htm
tech.root: gdi
ms.assetid: ec5db6f9-93fa-4dbe-afdb-c039292b26e3
ms.date: 12/05/2018
ms.keywords: '*LPBITMAPV5HEADER, *PBITMAPV5HEADER, BITMAPV5HEADER, BITMAPV5HEADER structure [Windows GDI], PBITMAPV5HEADER, PBITMAPV5HEADER structure pointer [Windows GDI], _win32_BITMAPV5HEADER_str, gdi.bitmapv5header, wingdi/BITMAPV5HEADER, wingdi/PBITMAPV5HEADER'
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
req.typenames: BITMAPV5HEADER, *LPBITMAPV5HEADER, *PBITMAPV5HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPBITMAPV5HEADER
 - wingdi/LPBITMAPV5HEADER
 - BITMAPV5HEADER
 - wingdi/BITMAPV5HEADER
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
 - BITMAPV5HEADER
---

# BITMAPV5HEADER structure


## -description

The <b>BITMAPV5HEADER</b> structure is the bitmap information header file. It is an extended version of the <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

## -struct-fields

### -field bV5Size

The number of bytes required by the structure. Applications should use this member to determine which bitmap information header structure is being used.

### -field bV5Width

The width of the bitmap, in pixels.

If <b>bV5Compression</b> is BI_JPEG or BI_PNG, the <b>bV5Width</b> member specifies the width of the decompressed JPEG or PNG image in pixels.

### -field bV5Height

The height of the bitmap, in pixels. If the value of <b>bV5Height</b> is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner. If <b>bV5Height</b> value is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.

If <b>bV5Height</b> is negative, indicating a top-down DIB, <b>bV5Compression</b> must be either BI_RGB or BI_BITFIELDS. Top-down DIBs cannot be compressed.

If <b>bV5Compression</b> is BI_JPEG or BI_PNG, the <b>bV5Height</b> member specifies the height of the decompressed JPEG or PNG image in pixels.

### -field bV5Planes

The number of planes for the target device. This value must be set to 1.

### -field bV5BitCount

The number of bits that define each pixel and the maximum number of colors in the bitmap.

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>The number of bits per pixel is specified or is implied by the JPEG or PNG file format.</td>
</tr>
<tr>
<td>1</td>
<td>The bitmap is monochrome, and the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> contains two entries. Each bit in the bitmap array represents a pixel. If the bit is clear, the pixel is displayed with the color of the first entry in the <b>bmiColors</b> color table. If the bit is set, the pixel has the color of the second entry in the table.</td>
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
<td>The bitmap has a maximum of 2^16 colors. If the <b>bV5Compression</b> member of the <b>BITMAPV5HEADER</b> structure is BI_RGB, the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> is <b>NULL</b>. Each <b>WORD</b> in the bitmap array represents a single pixel. The relative intensities of red, green, and blue are represented with five bits for each color component. The value for blue is in the least significant five bits, followed by five bits each for green and red. The most significant bit is not used. The <b>bmiColors</b> color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the <b>bV5ClrUsed</b> member of the <b>BITMAPV5HEADER</b>.If the <b>bV5Compression</b> member of the <b>BITMAPV5HEADER</b> is BI_BITFIELDS, the <b>bmiColors</b> member contains three <b>DWORD</b> color masks that specify the red, green, and blue components, respectively, of each pixel. Each <b>WORD</b> in the bitmap array represents a single pixel.

When the <b>bV5Compression</b> member is BI_BITFIELDS, bits set in each <b>DWORD</b> mask must be contiguous and should not overlap the bits of another mask. All the bits in the pixel do not need to be used.

</td>
</tr>
<tr>
<td>24</td>
<td>The bitmap has a maximum of 2^24 colors, and the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> is <b>NULL</b>. Each 3-byte triplet in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel. The <b>bmiColors</b> color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the <b>bV5ClrUsed</b> member of the <b>BITMAPV5HEADER</b> structure.</td>
</tr>
<tr>
<td>32</td>
<td>The bitmap has a maximum of 2^32 colors. If the <b>bV5Compression</b> member of the <b>BITMAPV5HEADER</b> is BI_RGB, the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> is <b>NULL</b>. Each <b>DWORD</b> in the bitmap array represents the relative intensities of blue, green, and red for a pixel. The value for 
    blue is in the least significant 8 bits, followed by 8 bits each for green
    and red.  The high byte in each <b>DWORD</b> is not used. The <b>bmiColors</b> color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the <b>bV5ClrUsed</b> member of the <b>BITMAPV5HEADER</b>.If the <b>bV5Compression</b> member of the <b>BITMAPV5HEADER</b> is BI_BITFIELDS, the <b>bmiColors</b> member contains three <b>DWORD</b> color masks that specify the red, green, and blue components of each pixel. Each <b>DWORD</b> in the bitmap array represents a single pixel.

</td>
</tr>
</table>

### -field bV5Compression

Specifies that the bitmap is not compressed. The <b>bV5RedMask</b>, <b>bV5GreenMask</b>, and <b>bV5BlueMask</b> members specify the red, green, and blue components of each pixel. This is valid when used with 16- and 32-bpp bitmaps. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>BI_RGB</td>
<td>An uncompressed format.</td>
</tr>
<tr>
<td>BI_RLE8</td>
<td>A run-length encoded (RLE) format for bitmaps with 8 bpp. The compression format is a two-byte format consisting of a count byte followed by a byte containing a color index. If <b>bV5Compression</b> is BI_RGB and the <b>bV5BitCount</b> member is 16, 24, or 32, the bitmap array specifies the actual intensities of blue, green, and red rather than using color table indexes. For more information, see <a href="/windows/desktop/gdi/bitmap-compression">Bitmap Compression</a>.</td>
</tr>
<tr>
<td>BI_RLE4</td>
<td>An RLE format for bitmaps with 4 bpp. The compression format is a two-byte format consisting of a count byte followed by two word-length color indexes. For more information, see <a href="/windows/desktop/gdi/bitmap-compression">Bitmap Compression</a>.</td>
</tr>
<tr>
<td>BI_BITFIELDS</td>
<td>Specifies that the bitmap is not compressed and that the color masks for the red, green, and blue components of each pixel are specified in the <b>bV5RedMask</b>, <b>bV5GreenMask</b>, and <b>bV5BlueMask</b> members. This is valid when used with 16- and 32-bpp bitmaps.</td>
</tr>
<tr>
<td>BI_JPEG</td>
<td>Specifies that the image is compressed using the JPEG file Interchange Format. JPEG compression trades off compression against loss; it can achieve a compression ratio of 20:1 with little noticeable loss.</td>
</tr>
<tr>
<td>BI_PNG</td>
<td>Specifies that the image is compressed using the PNG file Interchange Format.</td>
</tr>
</table>

### -field bV5SizeImage

The size, in bytes, of the image. This may be set to zero for BI_RGB bitmaps.

If <b>bV5Compression</b> is BI_JPEG or BI_PNG, <b>bV5SizeImage</b> is the size of the JPEG or PNG image buffer.

### -field bV5XPelsPerMeter

The horizontal resolution, in pixels-per-meter, of the target device for the bitmap. An application can use this value to select a bitmap from a resource group that best matches the characteristics of the current device.

### -field bV5YPelsPerMeter

The vertical resolution, in pixels-per-meter, of the target device for the bitmap.

### -field bV5ClrUsed

The number of color indexes in the color table that are actually used by the bitmap. If this value is zero, the bitmap uses the maximum number of colors corresponding to the value of the <b>bV5BitCount</b> member for the compression mode specified by <b>bV5Compression</b>.

If <b>bV5ClrUsed</b> is nonzero and <b>bV5BitCount</b> is less than 16, the <b>bV5ClrUsed</b> member specifies the actual number of colors the graphics engine or device driver accesses. If <b>bV5BitCount</b> is 16 or greater, the <b>bV5ClrUsed</b> member specifies the size of the color table used to optimize performance of the system color palettes. If <b>bV5BitCount</b> equals 16 or 32, the optimal color palette starts immediately following the <b>BITMAPV5HEADER</b>. If <b>bV5ClrUsed</b> is nonzero, the color table is used on palettized devices, and <b>bV5ClrUsed</b> specifies the number of entries.

### -field bV5ClrImportant

The number of color indexes that are required for displaying the bitmap. If this value is zero, all colors are required.

### -field bV5RedMask

Color mask that specifies the red component of each pixel, valid only if <b>bV5Compression</b> is set to BI_BITFIELDS.

### -field bV5GreenMask

Color mask that specifies the green component of each pixel, valid only if <b>bV5Compression</b> is set to BI_BITFIELDS.

### -field bV5BlueMask

Color mask that specifies the blue component of each pixel, valid only if <b>bV5Compression</b> is set to BI_BITFIELDS.

### -field bV5AlphaMask

Color mask that specifies the alpha component of each pixel.

### -field bV5CSType

The color space of the DIB.

The following table specifies the values for <b>bV5CSType</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>LCS_CALIBRATED_RGB</td>
<td>This value implies that endpoints and gamma values are given in the appropriate fields.</td>
</tr>
<tr>
<td>LCS_sRGB</td>
<td>Specifies that the bitmap is in sRGB color space.</td>
</tr>
<tr>
<td>LCS_WINDOWS_COLOR_SPACE</td>
<td>This value indicates that the bitmap is in the system default color space, sRGB.</td>
</tr>
<tr>
<td>PROFILE_LINKED</td>
<td>This value indicates that <b>bV5ProfileData</b> points to the file name of the profile to use (gamma and endpoints values are ignored).</td>
</tr>
<tr>
<td>PROFILE_EMBEDDED</td>
<td>This value indicates that <b>bV5ProfileData</b> points to a memory buffer that contains the profile to be used (gamma and endpoints values are ignored).</td>
</tr>
</table>
 

See the <a href="/windows/desktop/api/wingdi/ns-wingdi-logcolorspacea">LOGCOLORSPACE</a> structure for information that defines a logical color space.

### -field bV5Endpoints

A <a href="/windows/win32/api/wingdi/ns-wingdi-ciexyztriple">CIEXYZTRIPLE</a> structure that specifies the x, y, and z coordinates of the three colors that correspond to the red, green, and blue endpoints for the logical color space associated with the bitmap. This member is ignored unless the <b>bV5CSType</b> member specifies LCS_CALIBRATED_RGB.

### -field bV5GammaRed

Toned response curve for red. Used if <b>bV5CSType</b> is set to LCS_CALIBRATED_RGB. Specify in unsigned fixed 16.16 format. The upper 16 bits are the unsigned integer value. The lower 16 bits are the fractional part.

### -field bV5GammaGreen

Toned response curve for green. Used if <b>bV5CSType</b> is set to LCS_CALIBRATED_RGB. Specify in unsigned fixed 16.16 format. The upper 16 bits are the unsigned integer value. The lower 16 bits are the fractional part.

### -field bV5GammaBlue

Toned response curve for blue. Used if <b>bV5CSType</b> is set to LCS_CALIBRATED_RGB. Specify in unsigned fixed 16.16 format. The upper 16 bits are the unsigned integer value. The lower 16 bits are the fractional part.

### -field bV5Intent

Rendering intent for bitmap. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Intent</th>
<th>ICC name</th>
<th>Meaning</th>
</tr>
<tr>
<td>LCS_GM_ABS_COLORIMETRIC</td>
<td>Match</td>
<td>Absolute Colorimetric</td>
<td>Maintains the white point. Matches the colors to their nearest color in the destination gamut.</td>
</tr>
<tr>
<td>LCS_GM_BUSINESS</td>
<td>Graphic</td>
<td>Saturation</td>
<td>Maintains saturation. Used for business charts and other situations in which undithered colors are required.</td>
</tr>
<tr>
<td>LCS_GM_GRAPHICS</td>
<td>Proof</td>
<td>Relative Colorimetric</td>
<td>Maintains colorimetric match. Used for graphic designs and named colors.</td>
</tr>
<tr>
<td>LCS_GM_IMAGES</td>
<td>Picture</td>
<td>Perceptual</td>
<td>Maintains contrast. Used for photographs and natural images.</td>
</tr>
</table>

### -field bV5ProfileData

The offset, in bytes, from the beginning of the <b>BITMAPV5HEADER</b> structure to the start of the profile data. If the profile is embedded, profile data is the actual profile, and it is linked. (The profile data is the null-terminated file name of the profile.) This cannot be a Unicode string. It must be composed exclusively of characters from the Windows character set (code page 1252). These profile members are ignored unless the <b>bV5CSType</b> member specifies PROFILE_LINKED or PROFILE_EMBEDDED.

### -field bV5ProfileSize

Size, in bytes, of embedded profile data.

### -field bV5Reserved

This member has been reserved. Its value should be set to zero.

## -remarks

If <b>bV5Height</b> is negative, indicating a top-down DIB, <b>bV5Compression</b> must be either BI_RGB or BI_BITFIELDS. Top-down DIBs cannot be compressed.

The Independent Color Management interface (ICM) 2.0 allows International Color Consortium (ICC) color profiles to be linked or embedded in DIBs (DIBs). See <a href="/windows/win32/wcs/using-structures-in-wcs-1-0">Using Structures</a> for more information.

When a DIB is loaded into memory, the profile data (if present) should follow the color table, and the <b>bV5ProfileData</b> should provide the offset of the profile data from the beginning of the <b>BITMAPV5HEADER</b> structure. The value stored in <b>bV5ProfileData</b> will be different from the value returned by the <b>sizeof</b> operator given the <b>BITMAPV5HEADER</b> argument, because <b>bV5ProfileData</b> is the offset in bytes from the beginning of the <b>BITMAPV5HEADER</b> structure to the start of the profile data. (Bitmap bits do not follow the color table in memory). Applications should modify the <b>bV5ProfileData</b> member after loading the DIB into memory.

For packed DIBs, the profile data should follow the bitmap bits similar to the file format. The <b>bV5ProfileData</b> member should still give the offset of the profile data from the beginning of the <b>BITMAPV5HEADER</b>.

Applications should access the profile data only when <b>bV5Size</b> equals the size of the <b>BITMAPV5HEADER</b> and <b>bV5CSType</b> equals PROFILE_EMBEDDED or PROFILE_LINKED.

If a profile is linked, the path of the profile can be any fully qualified name (including a network path) that can be opened using the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv4header">BITMAPV4HEADER</a>



<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-ciexyztriple">CIEXYZTRIPLE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logcolorspacea">LOGCOLORSPACE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>

