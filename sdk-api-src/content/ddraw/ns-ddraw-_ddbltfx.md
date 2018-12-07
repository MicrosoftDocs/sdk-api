---
UID: NS:ddraw._DDBLTFX
title: "_DDBLTFX"
author: windows-sdk-content
description: The DDBLTFX structure passes raster operations (ROPs), effects, and override information to the IDirectDrawSurface7::Blt method. This structure is also part of the DDBLTBATCH structure that is used with the IDirectDrawSurface7::BltBatch method.
old-location: directdraw\ddbltfx.htm
tech.root: directdraw
ms.assetid: a542434f-61d3-4c73-a087-ffb83a509c67
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDDBLTFX, DDBLTFX, DDBLTFX structure [DirectDraw], DDBLTFX_ARITHSTRETCHY, DDBLTFX_MIRRORLEFTRIGHT, DDBLTFX_MIRRORUPDOWN, DDBLTFX_NOTEARING, DDBLTFX_ROTATE180, DDBLTFX_ROTATE270, DDBLTFX_ROTATE90, DDBLTFX_ZBUFFERBASEDEST, DDBLTFX_ZBUFFERRANGE, LPDDBLTFX, LPDDBLTFX structure pointer [DirectDraw], _DDBLTFX, ddraw/DDBLTFX, ddraw/LPDDBLTFX, directdraw.ddbltfx"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddraw.h
api_name:
 - DDBLTFX
product: Windows
targetos: Windows
req.typenames: DDBLTFX
req.redist: 
---

# _DDBLTFX structure


## -description


The DDBLTFX structure passes raster operations (ROPs), effects, and override information to the <a href="https://msdn.microsoft.com/e458c430-855c-419b-aa50-144d2b422e78">IDirectDrawSurface7::Blt</a> method. This structure is also part of the <a href="https://msdn.microsoft.com/d8c302aa-9c57-41f8-ad22-d8fdd1158c3c">DDBLTBATCH</a> structure that is used with the <a href="https://msdn.microsoft.com/50c071a6-2963-474e-994e-c789b1924d92">IDirectDrawSurface7::BltBatch</a> method.




## -struct-fields




### -field dwSize

Size of the structure, in bytes. This member must be initialized before the structure is used.


### -field dwDDFX

Type of FX operations. The following types are defined:



#### DDBLTFX_ARITHSTRETCHY

Uses arithmetic stretching along the y-axis for this bit block transfer (bitblt).



#### DDBLTFX_MIRRORLEFTRIGHT

Turns the surface on its y-axis. This bitblt mirrors the surface from left to right.



#### DDBLTFX_MIRRORUPDOWN

Turns the surface on its x-axis. This bitblt mirrors the surface from top to bottom.



#### DDBLTFX_NOTEARING

Schedules this bitblt to avoid tearing.



#### DDBLTFX_ROTATE180

Rotates the surface 180 degrees clockwise during this bitblt.



#### DDBLTFX_ROTATE270

Rotates the surface 270 degrees clockwise during this bitblt.



#### DDBLTFX_ROTATE90

Rotates the surface 90 degrees clockwise during this bitblt.



#### DDBLTFX_ZBUFFERBASEDEST

Adds the <b>dwZBufferBaseDest</b> member to each of the source z-values before comparing them with the destination z-values during this z-bitblt.



#### DDBLTFX_ZBUFFERRANGE

Uses the <b>dwZBufferLow</b> and <b>dwZBufferHigh</b> members as range values to specify limits to the bits copied from a source surface during this z-bitblt.


### -field dwROP

Win32 raster operations. You can retrieve a list of supported raster operations by calling the <a href="https://msdn.microsoft.com/4e93612c-9e28-4d51-a640-e8e9b5ed8e7a">IDirectDraw7::GetCaps</a> method.


### -field dwDDROP

DirectDraw raster operations.


### -field dwRotationAngle

Rotation angle for the bitblt.


### -field dwZBufferOpCode

Z-buffer compares.


### -field dwZBufferLow

Low limit of a z-buffer.


### -field dwZBufferHigh

High limit of a z-buffer.


### -field dwZBufferBaseDest

Destination base value of a z-buffer.


### -field dwZDestConstBitDepth

Bit depth of the destination z-constant.


### -field DUMMYUNIONNAMEN.dwZDestConst

 


### -field DUMMYUNIONNAMEN.lpDDSZBufferDest

 


### -field dwZSrcConstBitDepth

Bit depth of the source z-constant.


### -field DUMMYUNIONNAMEN.dwZSrcConst

 


### -field DUMMYUNIONNAMEN.lpDDSZBufferSrc

 


### -field dwAlphaEdgeBlendBitDepth

Bit depth of the constant for an alpha edge blend.


### -field dwAlphaEdgeBlend

Alpha constant used for edge blending.


### -field dwReserved

Reserved


### -field dwAlphaDestConstBitDepth

Bit depth of the destination alpha constant.


### -field DUMMYUNIONNAMEN.dwAlphaDestConst

 


### -field DUMMYUNIONNAMEN.lpDDSAlphaDest

 


### -field dwAlphaSrcConstBitDepth

Bit depth of the source alpha constant.


### -field DUMMYUNIONNAMEN.dwAlphaSrcConst

 


### -field DUMMYUNIONNAMEN.lpDDSAlphaSrc

 


### -field DUMMYUNIONNAMEN

 


### -field DUMMYUNIONNAMEN.dwFillColor

 


### -field DUMMYUNIONNAMEN.dwFillDepth

 


### -field DUMMYUNIONNAMEN.dwFillPixel

 


### -field DUMMYUNIONNAMEN.lpDDSPattern

 


### -field ddckDestColorkey

Destination color key override.


### -field ddckSrcColorkey

Source color key override.


#### - DUMMYUNIONNAMEN(1)



#### dwZDestConst

Constant used as the z-buffer destination.



#### lpDDSZBufferDest

Surface used as the z-buffer destination.


#### - DUMMYUNIONNAMEN(2)



#### dwZSrcConst

Constant used as the z-buffer destination.



#### lpDDSZBufferSrc

Surface used as the z-buffer source.


#### - DUMMYUNIONNAMEN(3)



#### dwAlphaDestConst

Constant used as the alpha channel destination.



#### lpDDSAlphaDest

Surface used as the alpha channel destination.


#### - DUMMYUNIONNAMEN(4)



#### dwAlphaSrcConst

Constant used as the alpha channel source.



#### lpDDSAlphaSrc

Surface used as the alpha channel source.


#### - DUMMYUNIONNAMEN(5)



#### dwFillColor

Color used to fill a surface when DDBLT_COLORFILL is specified. This value must be a pixel appropriate to the pixel format of the destination surface. For a palettized surface, it would be a palette index, and for a 16-bit RGB surface, it would be a 16-bit pixel value.



#### dwFillDepth

Depth value for the z-buffer.



#### dwFillPixel

Pixel value for RGBA or RGBZ fills. Applications that use RGBZ fills should use this member, not <b>dwFillColor</b> or <b>dwFillDepth</b>.



#### lpDDSPattern

Surface to use as a pattern. The pattern can be used in certain blit operations that combine a source and a destination.


## -remarks



The unions in this structure have been updated to work with compilers that do not support nameless unions. If your compiler does not support nameless unions, define the NONAMELESSUNION token before including the Ddraw.h header file.





