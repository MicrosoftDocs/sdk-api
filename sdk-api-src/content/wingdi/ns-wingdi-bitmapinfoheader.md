---
UID: NS:wingdi.tagBITMAPINFOHEADER
title: BITMAPINFOHEADER (wingdi.h)
description: The BITMAPINFOHEADER structure contains information about the dimensions and color format of a device-independent bitmap (DIB).
helpviewer_keywords: ["*LPBITMAPINFOHEADER","*PBITMAPINFOHEADER","BITMAPINFOHEADER","BITMAPINFOHEADER structure [DirectShow]","BITMAPINFOHEADER structure [Windows GDI]","BITMAPINFOHEADERStructure","BI_BITFIELDS","BI_JPEG","BI_PNG","BI_RGB","BI_RLE4","BI_RLE8","dshow.bitmapinfoheader","gdi.bitmapinfoheader","tagBITMAPINFOHEADER","wingdi/BITMAPINFOHEADER"]
old-location: dshow\bitmapinfoheader.htm
tech.root: gdi
ms.assetid: 153c08a8-d32c-4e9d-9da9-b915eb172327
ms.date: 4/26/2023
ms.keywords: '*LPBITMAPINFOHEADER, *PBITMAPINFOHEADER, BITMAPINFOHEADER, BITMAPINFOHEADER structure [DirectShow], BITMAPINFOHEADER structure [Windows GDI], BITMAPINFOHEADERStructure, BI_BITFIELDS, BI_JPEG, BI_PNG, BI_RGB, BI_RLE4, BI_RLE8, dshow.bitmapinfoheader, gdi.bitmapinfoheader, tagBITMAPINFOHEADER, wingdi/BITMAPINFOHEADER'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: BITMAPINFOHEADER, *LPBITMAPINFOHEADER, *PBITMAPINFOHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagBITMAPINFOHEADER
 - wingdi/tagBITMAPINFOHEADER
 - LPBITMAPINFOHEADER
 - wingdi/LPBITMAPINFOHEADER
 - BITMAPINFOHEADER
 - wingdi/BITMAPINFOHEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinGDI.h
api_name:
 - BITMAPINFOHEADER
---

# BITMAPINFOHEADER structure

## -description

The <b>BITMAPINFOHEADER</b> structure contains information about the dimensions and color format of a device-independent bitmap (DIB).

## -struct-fields

### -field biSize

The number of bytes required by the structure. This value does not include the size of the color table or the size of the color masks, if they are appended to the end of the structure.

### -field biWidth

The width of the bitmap, in pixels.

If <b>biCompression</b> is BI_JPEG or BI_PNG, the <b>biWidth</b> member specifies the width of the decompressed JPEG or PNG image file, respectively.

### -field biHeight

The height of the bitmap, in pixels. If <b>biHeight</b> is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner. If <b>biHeight</b> is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.

If <b>biHeight</b> is negative, indicating a top-down DIB, <b>biCompression</b> must be either BI_RGB or BI_BITFIELDS. Top-down DIBs cannot be compressed.

If <b>biCompression</b> is BI_JPEG or BI_PNG, the <b>biHeight</b> member specifies the height of the decompressed JPEG or PNG image file, respectively.

### -field biPlanes

The number of planes for the target device. This value must be set to 1.

### -field biBitCount

The number of bits-per-pixel. The <b>biBitCount</b> member of the <b>BITMAPINFOHEADER</b> structure determines the number of bits that define each pixel and the maximum number of colors in the bitmap. This member must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>The number of bits-per-pixel is specified or is implied by the JPEG or PNG format.</td>
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
<td>The bitmap has a maximum of 2^16 colors. If the <b>biCompression</b> member of the <b>BITMAPINFOHEADER</b> is BI_RGB, the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> is <b>NULL</b>. Each <b>WORD</b> in the bitmap array represents a single pixel. The relative intensities of red, green, and blue are represented with five bits for each color component. The value for blue is in the least significant five bits, followed by five bits each for green and red. The most significant bit is not used. The <b>bmiColors</b> color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the <b>biClrUsed</b> member of the <b>BITMAPINFOHEADER</b>.

If the <b>biCompression</b> member of the <b>BITMAPINFOHEADER</b> is BI_BITFIELDS, the <b>bmiColors</b> member contains three <b>DWORD</b> color masks that specify the red, green, and blue components, respectively, of each pixel. Each <b>WORD</b> in the bitmap array represents a single pixel.

When the <b>biCompression</b> member is BI_BITFIELDS, bits set in each <b>DWORD</b> mask must be contiguous and should not overlap the bits of another mask. All the bits in the pixel do not have to be used.</td>
</tr>
<tr>
<td>24</td>
<td>The bitmap has a maximum of 2^24 colors, and the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> is <b>NULL</b>. Each 3-byte triplet in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel. The <b>bmiColors</b> color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the <b>biClrUsed</b> member of the <b>BITMAPINFOHEADER</b>.</td>
</tr>
<tr>
<td>32</td>
<td>The bitmap has a maximum of 2^32 colors. If the <b>biCompression</b> member of the <b>BITMAPINFOHEADER</b> is BI_RGB, the <b>bmiColors</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> is <b>NULL</b>. Each <b>DWORD</b> in the bitmap array represents the relative intensities of blue, green, and red for a pixel. The value for blue is in the least significant 8 bits, followed by 8 bits each for green and red. The high byte in each <b>DWORD</b> is not used. The <b>bmiColors</b> color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the <b>biClrUsed</b> member of the <b>BITMAPINFOHEADER</b>.

If the <b>biCompression</b> member of the <b>BITMAPINFOHEADER</b> is BI_BITFIELDS, the <b>bmiColors</b> member contains three <b>DWORD</b> color masks that specify the red, green, and blue components, respectively, of each pixel. Each <b>DWORD</b> in the bitmap array represents a single pixel.

When the <b>biCompression</b> member is BI_BITFIELDS, bits set in each <b>DWORD</b> mask must be contiguous and should not overlap the bits of another mask. All the bits in the pixel do not need to be used.</td>
</tr>
</table>

### -field biCompression

The type of compression for a compressed bottom-up bitmap (top-down DIBs cannot be compressed). This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><a id="BI_RGB"></a><a id="bi_rgb"></a><b>BI_RGB</b></td>
<td>An uncompressed format.</td>
</tr>
<tr>
<td><b>BI_RLE8</b></td>
<td>A run-length encoded (RLE) format for bitmaps with 8 bpp. The compression format is a 2-byte format consisting of a count byte followed by a byte containing a color index. For more information, see <a href="/windows/desktop/gdi/bitmap-compression">Bitmap Compression</a>.</td>
</tr>
<tr>
<td><b>BI_RLE4</b></td>
<td>An RLE format for bitmaps with 4 bpp. The compression format is a 2-byte format consisting of a count byte followed by two word-length color indexes. For more information, see <a href="/windows/desktop/gdi/bitmap-compression">Bitmap Compression</a>.</td>
</tr>
<tr>
<td><a id="BI_BITFIELDS"></a><a id="bi_bitfields"></a><b>BI_BITFIELDS</b></td>
<td>Specifies that the bitmap is not compressed and that the color table consists of three <b>DWORD</b> color masks that specify the red, green, and blue components, respectively, of each pixel. This is valid when used with 16- and 32-bpp bitmaps.</td>
</tr>
<tr>
<td><b>BI_JPEG</b></td>
<td>Indicates that the image is a JPEG image.</td>
</tr>
<tr>
<td><b>BI_PNG</b></td>
<td>Indicates that the image is a PNG image.</td>
</tr>
</table>

### -field biSizeImage

The size, in bytes, of the image. This may be set to zero for BI_RGB bitmaps.

If <b>biCompression</b> is BI_JPEG or BI_PNG, <b>biSizeImage</b> indicates the size of the JPEG or PNG image buffer, respectively.

### -field biXPelsPerMeter

The horizontal resolution, in pixels-per-meter, of the target device for the bitmap. An application can use this value to select a bitmap from a resource group that best matches the characteristics of the current device.

### -field biYPelsPerMeter

The vertical resolution, in pixels-per-meter, of the target device for the bitmap.

### -field biClrUsed

The number of color indexes in the color table that are actually used by the bitmap. If this value is zero, the bitmap uses the maximum number of colors corresponding to the value of the <b>biBitCount</b> member for the compression mode specified by <b>biCompression</b>.

If <b>biClrUsed</b> is nonzero and the <b>biBitCount</b> member is less than 16, the <b>biClrUsed</b> member specifies the actual number of colors the graphics engine or device driver accesses. If <b>biBitCount</b> is 16 or greater, the <b>biClrUsed</b> member specifies the size of the color table used to optimize performance of the system color palettes. If <b>biBitCount</b> equals 16 or 32, the optimal color palette starts immediately following the three <b>DWORD</b> masks.

When the bitmap array immediately follows the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure, it is a packed bitmap. Packed bitmaps are referenced by a single pointer. Packed bitmaps require that the <b>biClrUsed</b> member must be either zero or the actual size of the color table.

### -field biClrImportant

The number of color indexes that are required for displaying the bitmap. If this value is zero, all colors are required.

## -remarks

The <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure combines the <b>BITMAPINFOHEADER</b> structure and a color table to provide a complete definition of the dimensions and colors of a DIB. For more information about DIBs, see <a href="/windows/desktop/gdi/device-independent-bitmaps">Device-Independent Bitmaps</a> and <b>BITMAPINFO</b>.

An application should use the information stored in the <b>biSize</b> member to locate the color table in a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure, as follows:

```cpp
pColor = ((LPSTR)pBitmapInfo + (WORD)(pBitmapInfo->bmiHeader.biSize));
```

If <b>biCompression</b> equals <b>BI_RGB</b> and <b>biBitCount</b> is 8 bpp or less, an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a> values immediately follows the <b>BITMAPINFOHEADER</b> structure. The number of entries in the array is given by <b>biClrUsed</b>, or by 2^<b>biBitCount</b> if <b>biClrUsed</b> is zero. If <b>biCompression</b> equals <b>BI_BITFIELDS</b>, three <b>DWORD</b> color masks (red, green, and blue, in that order) immediately follow the structure instead.

When a color table or color masks follow the <b>BITMAPINFOHEADER</b> structure, you can cast or copy the combined memory block to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure, where <b>bmiHeader</b> is the <b>BITMAPINFOHEADER</b> structure and <b>bmiColors</b> is the first entry in the color table or the first color mask.

```cpp
typedef struct tagBITMAPINFO {
    BITMAPINFOHEADER bmiHeader;
    RGBQUAD          bmiColors[1];
} BITMAPINFO;
```

Because the color table or color masks are appended after the fixed part of the structure, the actual size of the format block is not necessarily equal to <b>sizeof(BITMAPINFOHEADER)</b> or <b>sizeof(BITMAPINFO)</b>. Calculate the actual size for each instance rather than assuming one of these fixed sizes.

The <b>BITMAPINFOHEADER</b> structure is extended to allow a JPEG or PNG image to be passed as the source image to <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>.

In an uncompressed bitmap, the stride is the number of bytes needed to go from the start of one row of pixels to the start of the next row. For uncompressed RGB formats, the minimum stride is always the image width in bytes, rounded up to the nearest <b>DWORD</b>. To calculate the stride and image size, you can use the <b>GDI_DIBWIDTHBYTES</b> and/or <b>GDI_DIBSIZE</b> macros, or the following formula:

```cpp
stride = ((((biWidth * biBitCount) + 31) & ~31) >> 3);
biSizeImage = abs(biHeight) * stride;
```

The graphics hardware might require a larger stride for the surface that contains the image than this minimum. If there is padding in the image buffer, never dereference a pointer into the memory that has been reserved for the padding. If the image buffer has been allocated in video memory, the padding might not be readable memory.

<h3><a id="Use_with_DirectShow_and_video_formats"></a><a id="use_with_directshow_and_video_formats"></a><a id="USE_WITH_DIRECTSHOW_AND_VIDEO_FORMATS"></a>Use with DirectShow and video formats</h3>

\[The feature associated with this section, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<b>BITMAPINFOHEADER</b> is also used to describe DirectShow video formats. The semantics for video data are slightly different than the semantics used elsewhere in this topic. If you are using this structure to describe video data, use the information given here instead.

<ul>
<li>For compressed video and YUV formats, <b>biCompression</b> is a FOURCC code, specified as a <b>DWORD</b> in little-endian order. For example, YUYV video has the FOURCC 'VYUY' or 0x56595559. For more information, see <a href="/windows/desktop/DirectShow/fourcc-codes">FOURCC Codes</a>. Note that <b>BI_JPEG</b> and <b>BI_PNG</b> are not valid video formats.</li>
<li>For 16-bpp video bitmaps, if <b>biCompression</b> equals <b>BI_RGB</b>, the format is always RGB 555. If <b>biCompression</b> equals <b>BI_BITFIELDS</b>, the format is either RGB 555 or RGB 565. Use the subtype GUID in the <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure to determine the specific RGB type.</li>
<li>For uncompressed RGB video bitmaps, if <b>biHeight</b> is positive, the bitmap is a bottom-up DIB with the origin at the lower left corner; if <b>biHeight</b> is negative, the bitmap is a top-down DIB with the origin at the upper left corner. For YUV bitmaps, the bitmap is always top-down, regardless of the sign of <b>biHeight</b>. Decoders should offer YUV formats with positive <b>biHeight</b>, but for backward compatibility they should accept YUV formats with either positive or negative <b>biHeight</b>. For compressed formats, <b>biHeight</b> must be positive, regardless of image orientation.</li>
<li>For uncompressed formats, <b>biBitCount</b> is the average number of bits per pixel. For compressed formats, <b>biBitCount</b> is the implied bit depth of the uncompressed image, after the image has been decoded.</li>
<li>If <b>biCompression</b> is a video FOURCC, the presence of a color table is implied by the video format. You should not assume that a color table exists when the bit depth is 8 bpp or less. However, some legacy components might assume that a color table is present. Therefore, if you are allocating a <b>BITMAPINFOHEADER</b> structure, it is recommended to allocate space for a color table when the bit depth is 8 bpp or less, even if the color table is not used.</li>
</ul>

<h4>Calculating surface stride for video</h4>

For YUV formats, there is no general rule for calculating the minimum stride. You must understand the rules for the particular YUV format. For a description of the most common YUV formats, see <a href="/windows/desktop/medfound/recommended-8-bit-yuv-formats-for-video-rendering">Recommended 8-Bit YUV Formats for Video Rendering</a>.

Decoders and video sources should propose formats where biWidth is the width of the image in pixels. If the video renderer requires a surface stride that is larger than the default image stride, it modifies the proposed media type by setting the following values:

<ul>
<li>It sets <b>biWidth</b> equal to the surface stride in pixels.</li>
<li>It sets the <b>rcTarget</b> member of the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> or <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2">VIDEOINFOHEADER2</a> structure equal to the image width, in pixels.</li>
</ul>
Then the video renderer proposes the modified format by calling <a href="/windows/desktop/api/strmif/nf-strmif-ipin-queryaccept">IPin::QueryAccept</a> on the upstream pin. For more information about this mechanism, see <a href="/windows/desktop/DirectShow/dynamic-format-changes">Dynamic Format Changes</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv4header">BITMAPV4HEADER</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header">BITMAPV5HEADER</a>



<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/device-independent-bitmaps">Device-Independent Bitmaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER Structure</a>



<a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2">VIDEOINFOHEADER2 Structure</a>



<a href="/windows/desktop/DirectShow/working-with-video-frames">Working with Video Frames</a>
