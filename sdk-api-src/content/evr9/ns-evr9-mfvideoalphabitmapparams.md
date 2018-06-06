---
UID: NS:evr9.MFVideoAlphaBitmapParams
title: MFVideoAlphaBitmapParams
author: windows-sdk-content
description: Specifies how the enhanced video renderer (EVR) alpha-blends a bitmap with the video.
old-location: mf\mfvideoalphabitmapparams.htm
old-project: medfound
ms.assetid: 3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce, MFVideoAlphaBitmapParams, MFVideoAlphaBitmapParams structure [Media Foundation], evr9/MFVideoAlphaBitmapParams, mf.mfvideoalphabitmapparams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFVideoAlphaBitmapParams
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - evr9.h
api_name:
 - MFVideoAlphaBitmapParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# MFVideoAlphaBitmapParams structure


## -description



Specifies how the enhanced video renderer (EVR) alpha-blends a bitmap with the video.




## -struct-fields




### -field dwFlags

Bitwise OR of one or more flags from the <a href="https://msdn.microsoft.com/d9989c44-8a3c-4f8b-a63d-e39e26797935">MFVideoAlphaBitmapFlags</a> enumeration. These flags indicate which of the other structure members contain valid information.


### -field clrSrcKey

Source color key. This member is used if the <b>dwFlags</b> member contains the MFVideoAlphaBitmap_SrcColorKey flag. Any pixels in the bitmap that match the color key are rendered as transparent pixels.

You cannot specify a color key if you are alpha-blending a Direct3D surface with per-pixel alpha (D3DFMT_A8R8G8B8).


### -field rcSrc

Source rectangle. The source rectangle defines the region of the bitmap that is alpha-blended with the video. The source rectangle is given in pixels and is relative to the original bitmap.

If you are alpha-blending a GDI bitmap, you must fill in this structure when you call <a href="https://msdn.microsoft.com/a70e6734-bf49-4dea-8bf6-917b8465cc78">IMFVideoMixerBitmap::SetAlphaBitmap</a>.

If you are alpha-blending a Direct3D surface and the <b>dwFlags</b> member contains the MFVideoAlphaBitmap_EntireDDS flag, the <b>rcSrc</b> member is ignored. If the flag is absent, you must fill in the <b>rcSrc</b> member.

After setting the initiali bitmap, you can update the source rectangle by calling <a href="https://msdn.microsoft.com/369bf934-b0a0-44b2-bea2-e8575404d36d">IMFVideoMixerBitmap::UpdateAlphaBitmapParameters</a>. To update the source rectangle, set the MFVideoAlphaBitmap_SrcColorKey flag in the <b>dwFlags</b> member.

The source rectangle cannot be an empty rectangle, and cannot exceed the bounds of the bitmap.


### -field nrcDest

Destination rectangle. The destination rectangle defines the region of the composited video image that receives the alpha-blended bitmap. The destination rectangle is specified as a normalized rectangle using the <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure.

This member is used if the <b>dwFlags</b> member contains the MFVideoAlphaBitmap_DestRect flag. Otherwise, the default destination rectangle is {0, 0, 1, 1}.


### -field fAlpha

Alpha blending value. This member is used if the <b>dwFlags</b> member contains the MFVideoAlphaBitmap_Alpha flag. Otherwise, the default value is 1.0 (opaque). The valid range is 0.0 to 1.0, inclusive.

This value is applied to the entire bitmap image. To create transparent regions, use the <b>clrSrcKey</b> member or use a DirectDraw surface with per-pixel alpha.


### -field dwFilterMode

Direct3D filtering mode to use when performing the alpha-blend operation. Specify the filter mode as a D3DTEXTUREFILTERTYPE value. For more information, see the Direct3D documentation.

This member is used if the <b>dwFlags</b> member contains the MFVideoAlphaBitmap_FilterMode flag. Otherwise, the default value is D3DTEXF_POINT.

Point filtering is particularly useful for images that contain text and will not be stretched.


## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/369bf934-b0a0-44b2-bea2-e8575404d36d">IMFVideoMixerBitmap::UpdateAlphaBitmapParameters</a>



<a href="https://msdn.microsoft.com/609041f2-7ba4-4157-819b-4ac21612dca2">MFVideoAlphaBitmap</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

