---
UID: NS:wingdi.tagBITMAPINFOHEADER
title: tagBITMAPINFOHEADER
author: windows-sdk-content
description: The BITMAPINFOHEADER structure contains information about the dimensions and color format of a device-independent bitmap (DIB).
old-location: dshow\bitmapinfoheader.htm
old-project: DirectShow
ms.assetid: 153c08a8-d32c-4e9d-9da9-b915eb172327
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: "*LPBITMAPINFOHEADER, *PBITMAPINFOHEADER, BITMAPINFOHEADER, BITMAPINFOHEADER structure [DirectShow], BITMAPINFOHEADERStructure, BI_BITFIELDS, BI_RGB, dshow.bitmapinfoheader, tagBITMAPINFOHEADER, wingdi/BITMAPINFOHEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BITMAPINFOHEADER, *LPBITMAPINFOHEADER, *PBITMAPINFOHEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinGDI.h
api_name:
 - BITMAPINFOHEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagBITMAPINFOHEADER structure


## -description


The <b>BITMAPINFOHEADER</b> structure contains information about the dimensions and color format of a device-independent bitmap (DIB).
<div class="alert"><b>Note</b>  This structure is also described in the GDI documentation. However, the semantics for video data are slightly different than the semantics used for GDI. If you are using this structure to describe video data, use the information given here.</div><div> </div>

## -struct-fields




### -field biSize

Specifies the number of bytes required by the structure. This value does not include the size of the color table or the size of the color masks, if they are appended to the end of structure. See Remarks.
          


### -field biWidth

Specifies the width of the bitmap, in pixels. For information about calculating the stride of the bitmap, see Remarks.
          


### -field biHeight

Specifies the height of the bitmap, in pixels.

<ul>
<li>For uncompressed RGB bitmaps, if <b>biHeight</b> is positive, the bitmap is a bottom-up DIB with the origin at the lower left corner. If <b>biHeight</b> is negative, the bitmap is a top-down DIB with the origin at the upper left corner.</li>
<li>For YUV bitmaps, the bitmap is always top-down, regardless of the sign of <b>biHeight</b>. Decoders should offer YUV formats with postive <b>biHeight</b>, but for backward compatibility they should accept YUV formats with either positive or negative <b>biHeight</b>.</li>
<li>For compressed formats, <b>biHeight</b> must be positive, regardless of image orientation.</li>
</ul>

### -field biPlanes

Specifies the number of planes for the target device. This value must be set to 1.
          


### -field biBitCount

Specifies the number of bits per pixel (bpp). For uncompressed formats, this value is the average number of bits per pixel. For compressed formats, this value is the implied bit depth of the uncompressed image, after the image has been decoded.
          


### -field biCompression

For compressed video and YUV formats, this member is a FOURCC code, specified as a <b>DWORD</b> in little-endian order. For example, YUYV video has the FOURCC 'VYUY' or 0x56595559. For more information, see <a href="https://msdn.microsoft.com/7627b580-4119-48e2-88b7-51b714b5d5b2">FOURCC Codes</a>.

For uncompressed RGB formats, the following values are possible:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BI_RGB"></a><a id="bi_rgb"></a><dl>
<dt><b>BI_RGB</b></dt>
</dl>
</td>
<td width="60%">
Uncompressed RGB. 

</td>
</tr>
<tr>
<td width="40%"><a id="BI_BITFIELDS"></a><a id="bi_bitfields"></a><dl>
<dt><b>BI_BITFIELDS</b></dt>
</dl>
</td>
<td width="60%">
Uncompressed RGB with color masks. Valid for 16-bpp and 32-bpp bitmaps.

</td>
</tr>
</table>
 

See Remarks for more information. Note that <b>BI_JPG</b> and <b>BI_PNG</b> are not valid video formats.

For 16-bpp bitmaps, if <b>biCompression</b> equals <b>BI_RGB</b>, the format is always RGB 555. If <b>biCompression</b> equals <b>BI_BITFIELDS</b>, the format is either RGB 555 or RGB 565. Use the subtype GUID in the <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure to determine the specific RGB type.


### -field biSizeImage

Specifies the size, in bytes, of the image. This can be set to 0 for uncompressed RGB bitmaps.
          


### -field biXPelsPerMeter

Specifies the horizontal resolution, in pixels per meter, of the target device for the bitmap.
          


### -field biYPelsPerMeter

Specifies the vertical resolution, in pixels per meter, of the target device for the bitmap.
          


### -field biClrUsed

Specifies the number of color indices in the color table that are actually used by the bitmap. See Remarks for more information.
          


### -field biClrImportant

Specifies the number of color indices that are considered important for displaying the bitmap. If this value is zero, all colors are important.
          


## -remarks



<h3><a id="Color_Tables"></a><a id="color_tables"></a><a id="COLOR_TABLES"></a>Color Tables</h3>
The <b>BITMAPINFOHEADER</b> structure may be followed by an array of palette entries or color masks. The rules depend on the value of <b>biCompression</b>.

<ul>
<li>If <b>biCompression</b> equals <b>BI_RGB</b> and the bitmap uses 8 bpp or less, the bitmap has a color table immediatelly following the <b>BITMAPINFOHEADER</b> structure. The color table consists of an array of <b>RGBQUAD</b> values. The size of the array is given by the <b>biClrUsed</b> member. If <b>biClrUsed</b> is zero, the array contains the maximum number of colors for the given bitdepth; that is, 2^<b>biBitCount</b> colors.</li>
<li>If <b>biCompression</b> equals <b>BI_BITFIELDS</b>, the bitmap uses three <b>DWORD</b> color masks (red, green, and blue, respectively), which specify the byte layout of the pixels. The 1 bits in each mask indicate the bits for that color within the pixel.</li>
<li>If <b>biCompression</b> is a video FOURCC, the presence of a color table is implied by the video format. You should not assume that a color table exists when the bit depth is 8 bpp or less. However, some legacy components might assume that a color table is present. Therefore, if you are allocating a <b>BITMAPINFOHEADER</b> structure, it is recommended to allocate space for a color table when the bit depth is 8 bpp or less, even if the color table is not used.</li>
</ul>
When the <b>BITMAPINFOHEADER</b> is followed by a color table or a set of color masks, you can use the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure to reference the color table of the color masks. The <b>BITMAPINFO</b> structure is defined as follows:

<pre class="syntax" xml:space="preserve"><code>typedef struct tagBITMAPINFO {
    BITMAPINFOHEADER bmiHeader;
    RGBQUAD          bmiColors[1];
} BITMAPINFO;
</code></pre>
If you cast the <b>BITMAPINFOHEADER</b> to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>, the <b>bmiHeader</b> member refers to the <b>BITMAPINFOHEADER</b> and the <b>bmiColors</b> member refers to the first entry in the color table, or the first color mask.

Be aware that if the bitmap uses a color table or color masks, then the size of the entire format structure (the <b>BITMAPINFOHEADER</b> plus the color information) is not equal to <code>sizeof(BITMAPINFOHEADER)</code> or <code>sizeof(BITMAPINFO)</code>. You must calculate the actual size for each instance.

<h3><a id="Calculating_Surface_Stride"></a><a id="calculating_surface_stride"></a><a id="CALCULATING_SURFACE_STRIDE"></a>Calculating Surface Stride</h3>
In an uncompressed bitmap, the stride is the number of bytes needed to go from the start of one row of pixels to the start of the next row. The image format defines a minimum stride for an image. In addition, the graphics hardware might require a larger stride for the surface that contains the image.

For uncompressed RGB formats, the minimum stride is always the image width in bytes, rounded up to the nearest <b>DWORD</b>. You can use the following formula to calculate the stride: 

<code>stride = ((((biWidth * biBitCount) + 31) &amp; ~31) &gt;&gt; 3)</code>

For YUV formats, there is no general rule for calculating the minimum stride. You must understand the rules for the particular YUV format. For a description of the most common YUV formats, see <a href="https://msdn.microsoft.com/675d4c60-4c58-4f15-9bae-ffb0c389c608">Recommended 8-Bit YUV Formats for Video Rendering</a>.

Decoders and video sources should propose formats where biWidth is the width of the image in pixels. If the video renderer requires a surface stride that is larger than the default image stride, it modifies the proposed media type by setting the following values:

<ul>
<li>It sets <b>biWidth</b> equal to the surface stride in pixels.</li>
<li>It sets the <b>rcTarget</b> member of the <a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER</a> or <a href="https://msdn.microsoft.com/5e3d5bf0-435f-45da-8409-a1463b56a7ae">VIDEOINFOHEADER2</a> structure equal to the image width, in pixels.</li>
</ul>
Then the video renderer proposes the modified format by calling <a href="https://msdn.microsoft.com/ed11eeef-464b-4a75-958b-2bc6dbc7af04">IPin::QueryAccept</a> on the upstream pin. For more information about this mechanism, see <a href="https://msdn.microsoft.com/ff60de5a-3edc-405d-aa02-8704b96d5e87">Dynamic Format Changes</a>.

If there is padding in the image buffer, never dereference a pointer into the memory that has been reserved for the padding. If the image buffer has been allocated in video memory, the padding might not be readable memory.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER Structure</a>



<a href="https://msdn.microsoft.com/5e3d5bf0-435f-45da-8409-a1463b56a7ae">VIDEOINFOHEADER2 Structure</a>



<a href="https://msdn.microsoft.com/a5ad74dd-abfd-4810-a512-42e4b98a6c59">Working with Video Frames</a>
 

 

