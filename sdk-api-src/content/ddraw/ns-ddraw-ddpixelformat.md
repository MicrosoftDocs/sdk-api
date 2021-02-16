---
UID: NS:ddraw._DDPIXELFORMAT
title: DDPIXELFORMAT (ddraw.h)
description: The DDPIXELFORMAT structure describes the pixel format of a DirectDrawSurface object for the IDirectDrawSurface7::GetPixelFormat method.
helpviewer_keywords: ["*LPDDPIXELFORMAT","DDPF_ALPHA","DDPF_ALPHAPIXELS","DDPF_ALPHAPREMULT","DDPF_BUMPDUDV","DDPF_BUMPLUMINANCE","DDPF_COMPRESSED","DDPF_D3DFORMAT","DDPF_FOURCC","DDPF_LUMINANCE","DDPF_PALETTEINDEXED1","DDPF_PALETTEINDEXED2","DDPF_PALETTEINDEXED4","DDPF_PALETTEINDEXED8","DDPF_PALETTEINDEXEDTO8","DDPF_RGB","DDPF_RGBTOYUV","DDPF_STENCILBUFFER","DDPF_YUV","DDPF_ZBUFFER","DDPF_ZPIXELS","DDPIXELFORMAT","DDPIXELFORMAT structure [DirectDraw]","LPDDPIXELFORMAT","LPDDPIXELFORMAT structure pointer [DirectDraw]","ddraw/DDPIXELFORMAT","ddraw/LPDDPIXELFORMAT","directdraw.ddpixelformat"]
old-location: directdraw\ddpixelformat.htm
tech.root: directdraw
ms.assetid: 17c531cb-7e65-482a-b3de-494874c1dd92
ms.date: 12/05/2018
ms.keywords: '*LPDDPIXELFORMAT, DDPF_ALPHA, DDPF_ALPHAPIXELS, DDPF_ALPHAPREMULT, DDPF_BUMPDUDV, DDPF_BUMPLUMINANCE, DDPF_COMPRESSED, DDPF_D3DFORMAT, DDPF_FOURCC, DDPF_LUMINANCE, DDPF_PALETTEINDEXED1, DDPF_PALETTEINDEXED2, DDPF_PALETTEINDEXED4, DDPF_PALETTEINDEXED8, DDPF_PALETTEINDEXEDTO8, DDPF_RGB, DDPF_RGBTOYUV, DDPF_STENCILBUFFER, DDPF_YUV, DDPF_ZBUFFER, DDPF_ZPIXELS, DDPIXELFORMAT, DDPIXELFORMAT structure [DirectDraw], LPDDPIXELFORMAT, LPDDPIXELFORMAT structure pointer [DirectDraw], ddraw/DDPIXELFORMAT, ddraw/LPDDPIXELFORMAT, directdraw.ddpixelformat'
req.header: ddraw.h
req.include-header: 
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
req.typenames: DDPIXELFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDPIXELFORMAT
 - ddraw/_DDPIXELFORMAT
 - DDPIXELFORMAT
 - ddraw/DDPIXELFORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddraw.h
api_name:
 - DDPIXELFORMAT
---

## -description

The <b>DDPIXELFORMAT</b> structure describes the pixel format of a DirectDrawSurface object for the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getpixelformat">IDirectDrawSurface7::GetPixelFormat</a> method.

<div class="alert"><b>Note</b>  Rather than use this structure to decode files with the DirectDraw Surface (DDS) file format (.dds), you should use an alternative structure that does not rely on Ddraw.h. For more information about alternative structures for DDS, see <a href="/windows/desktop/direct3ddds/dx-graphics-dds">DDS</a>.</div><div> </div>

## -struct-fields

### -field dwSize

Size of the structure, in bytes. This member must be initialized before the structure is used.

### -field dwFlags

The following flags to describe optional controls for this structure.

#### DDPF_ALPHA

The pixel format describes an alpha-only surface.

#### DDPF_ALPHAPIXELS

The surface has alpha channel information in the pixel format.

#### DDPF_ALPHAPREMULT

The surface uses the premultiplied alpha format. That is, the color components in each pixel are premultiplied by the alpha component.

#### DDPF_BUMPLUMINANCE

The luminance data in the pixel format is valid, and the <b>dwLuminanceBitMask</b> member describes valid luminance bits for a luminance-only or luminance-alpha surface.

#### DDPF_BUMPDUDV

Bump-map data in the pixel format is valid. Bump-map information is in the <b>dwBumpBitCount</b>, <b>dwBumpDuBitMask</b>, <b>dwBumpDvBitMask</b>, and <b>dwBumpLuminanceBitMask</b> members.

#### DDPF_COMPRESSED

The surface accepts pixel data in the specified format and compress it during the write operation.

#### DDPF_D3DFORMAT

Indicates a DirectX 8.0 and later format capability entry in the texture format list. This flag is not exposed to applications and is defined in Ddrawi.h.

#### DDPF_FOURCC

The <b>dwFourCC</b> member is valid and contains a FOURCC code that describes a non-RGB pixel format.

#### DDPF_LUMINANCE

The pixel format describes a luminance-only or luminance-alpha surface.

#### DDPF_PALETTEINDEXED1

The surface is 1-bit color-indexed.

#### DDPF_PALETTEINDEXED2

The surface is 2-bit color-indexed.

#### DDPF_PALETTEINDEXED4

The surface is 4-bit color-indexed.

#### DDPF_PALETTEINDEXED8

The surface is 8-bit color-indexed.

#### DDPF_PALETTEINDEXEDTO8

The surface is 1-, 2-, or 4-bit color-indexed to an 8-bit palette.

#### DDPF_RGB

The RGB data in the pixel format structure is valid.

#### DDPF_RGBTOYUV

The surface accepts RGB data and translates it during the write operation to YUV data. The format of the data to be written is contained in the pixel format structure. The DDPF_RGB flag is set.

#### DDPF_STENCILBUFFER

The surface encodes stencil and depth information in each pixel of the z-buffer. This flag can be used only if the DDPF_ZBUFFER flag is also specified.

#### DDPF_YUV

The YUV data in the pixel format structure is valid.

#### DDPF_ZBUFFER

The pixel format describes a z-buffer surface.

#### DDPF_ZPIXELS

The surface contains z information in the pixels.

### -field dwFourCC

A FourCC code.

### -field DUMMYUNIONNAMEN.dwRGBBitCount

RGB bits per pixel (4, 8, 16, 24, or 32).

### -field DUMMYUNIONNAMEN.dwYUVBitCount

YUV bits per pixel (4, 8, 16, 24, or 32).

### -field DUMMYUNIONNAMEN.dwZBufferBitDepth

Z-buffer bit depth (8, 16, 24, or 32).

### -field DUMMYUNIONNAMEN.dwAlphaBitDepth

Alpha channel bit depth (1, 2, 4, or 8) for an alpha-only surface (DDPF_ALPHA). For pixel formats that contain alpha information interleaved with color data (DDPF_ALPHAPIXELS), count the bits in the <b>dwRGBAlphaBitMask</b> member to obtain the bit depth of the alpha component. For more information about how to determine alpha bit depth, see Remarks.

### -field DUMMYUNIONNAMEN.dwLuminanceBitCount

Total luminance bits per pixel. This member applies only to luminance-only and luminance-alpha surfaces.

### -field DUMMYUNIONNAMEN.dwBumpBitCount

Total bump-map bits per pixel in a bump-map surface. 

### -field DUMMYUNIONNAMEN.dwPrivateFormatBitCount

Bits per pixel of private driver formats. Only valid in texture format list and if DDPF_D3DFORMAT is set.

### -field DUMMYUNIONNAMEN.dwRBitMask

Mask for red bits.

### -field DUMMYUNIONNAMEN.dwYBitMask

Mask for Y bits.

### -field DUMMYUNIONNAMEN.dwStencilBitDepth

Bit depth of the stencil buffer. This member specifies how many bits are reserved within each pixel of the z-buffer for stencil information (the total number of z-bits is equal to <b>dwZBufferBitDepth</b> minus <b>dwStencilBitDepth</b>). 

### -field DUMMYUNIONNAMEN.dwLuminanceBitMask

Mask for luminance bits.

### -field DUMMYUNIONNAMEN.dwBumpDuBitMask

Mask for bump-map U-delta bits.

### -field DUMMYUNIONNAMEN.dwOperations

Flags that specify the operations that can be performed on surfaces with the DDPF_D3DFORMAT pixel format. The flags are defined in Ddrawi.h.

### -field DUMMYUNIONNAMEN.dwGBitMask

Mask for green bits.

### -field DUMMYUNIONNAMEN.dwUBitMask

Mask for U bits.

### -field DUMMYUNIONNAMEN.dwZBitMask

Mask for z bits.

### -field DUMMYUNIONNAMEN.dwBumpDvBitMask

Mask for bump-map V-delta bits.

### -field DUMMYUNIONNAMEN.MultiSampleCaps

A structure that contains the following two members. This structure is used to specify surfaces that can be used when performing multisample rendering. Each bit in the 16-bit masks indicates support of multisampling with a specific number of samples. For example, bit 0 indicates support of multisampling with only a single sample, bit 1 indicates the support of multisampling with two samples, and so on. The driver can indicate more than one supported level by combining the bits by using a bitwise OR.

### -field DUMMYUNIONNAMEN.MultiSampleCaps.wFlipMSTypes

A 16-bit mask for full-screen (flip) mode multisampling.

### -field DUMMYUNIONNAMEN.MultiSampleCaps.wBltMSTypes

A 16-bit mask for windowed (bit-block transfer) mode multisampling.

### -field DUMMYUNIONNAMEN.dwBBitMask

Mask for blue bits.

### -field DUMMYUNIONNAMEN.dwVBitMask

Mask for V bits.

### -field DUMMYUNIONNAMEN.dwStencilBitMask

Mask for stencil bits within each z-buffer pixel.

### -field DUMMYUNIONNAMEN.dwBumpLuminanceBitMask

Mask for luminance in a bump-map pixel.

### -field DUMMYUNIONNAMEN.dwRGBAlphaBitMask

RGB mask for the alpha channel.

### -field DUMMYUNIONNAMEN.dwYUVAlphaBitMask

YUV mask for the alpha channel.

### -field DUMMYUNIONNAMEN.dwLuminanceAlphaBitMask

Luminance mask for the alpha channel.

### -field DUMMYUNIONNAMEN.dwRGBZBitMask

RGB mask for the z channel.

### -field DUMMYUNIONNAMEN.dwYUVZBitMask

YUV mask for the z channel.

## -remarks

The <b>dwAlphaBitDepth</b> member reflects the bit depth of an alpha-only pixel format (DDPF_ALPHA). For pixel formats that include the alpha component with color components (DDPF_ALPHAPIXELS), the alpha bit depth is obtained by counting the bits in the various mask members. The following code example returns the number of bits set in a given bitmask.

```cpp
WORD GetNumberOfBits( DWORD dwMask )
{
    WORD wBits = 0;
    while( dwMask )
    {
        dwMask = dwMask & ( dwMask - 1 );  
        wBits++;
    }
    return wBits;
}
```

The unions in <b>DDPIXELFORMAT</b> have been updated to work with compilers that do not support nameless unions. If your compiler does not support nameless unions, define the NONAMELESSUNION token before including the Ddraw.h header file.