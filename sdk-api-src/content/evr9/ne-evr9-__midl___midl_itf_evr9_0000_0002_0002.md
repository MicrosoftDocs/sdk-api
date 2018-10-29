---
UID: NE:evr9.__MIDL___MIDL_itf_evr9_0000_0002_0002
title: "__MIDL___MIDL_itf_evr9_0000_0002_0002"
author: windows-sdk-content
description: Defines flags for the MFVideoAlphaBitmapParams structure.
old-location: mf\mfvideoalphabitmapflags.htm
tech.root: medfound
ms.assetid: d9989c44-8a3c-4f8b-a63d-e39e26797935
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: MFVideoAlphaBitmapFlags, MFVideoAlphaBitmapFlags enumeration [Media Foundation], MFVideoAlphaBitmap_Alpha, MFVideoAlphaBitmap_BitMask, MFVideoAlphaBitmap_DestRect, MFVideoAlphaBitmap_EntireDDS, MFVideoAlphaBitmap_FilterMode, MFVideoAlphaBitmap_SrcColorKey, MFVideoAlphaBitmap_SrcRect, __MIDL___MIDL_itf_evr9_0000_0002_0002, d9989c44-8a3c-4f8b-a63d-e39e26797935, evr9/MFVideoAlphaBitmapFlags, evr9/MFVideoAlphaBitmap_Alpha, evr9/MFVideoAlphaBitmap_BitMask, evr9/MFVideoAlphaBitmap_DestRect, evr9/MFVideoAlphaBitmap_EntireDDS, evr9/MFVideoAlphaBitmap_FilterMode, evr9/MFVideoAlphaBitmap_SrcColorKey, evr9/MFVideoAlphaBitmap_SrcRect, mf.mfvideoalphabitmapflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - evr9.h
api_name:
 - MFVideoAlphaBitmapFlags
product: Windows
targetos: Windows
req.typenames: MFVideoAlphaBitmapFlags
req.redist: 
---

# __MIDL___MIDL_itf_evr9_0000_0002_0002 enumeration


## -description



Defines flags for the <a href="https://msdn.microsoft.com/3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce">MFVideoAlphaBitmapParams</a> structure.




## -enum-fields




### -field MFVideoAlphaBitmap_EntireDDS

Alpha-blend the entire DirectDraw suface.

If you are alpha-blending a DirectDraw surface, you can set this flag when you call <a href="https://msdn.microsoft.com/a70e6734-bf49-4dea-8bf6-917b8465cc78">IMFVideoMixerBitmap::SetAlphaBitmap</a>. If this flag is set, the mixer ignores the <b>rcSrc</b> member of the <a href="https://msdn.microsoft.com/3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce">MFVideoAlphaBitmapParams</a> structure. If this flag is absent, the <b>rcSrc</b> member specifies the source rectangle.

This flag cannot be used if you specify a GDI bitmap for alpha-blending. For a GDI bitmap, you must fill in the <b>rcSrc</b> member when you call <a href="https://msdn.microsoft.com/a70e6734-bf49-4dea-8bf6-917b8465cc78">SetAlphaBitmap</a>.

This flag does not apply to the <a href="https://msdn.microsoft.com/369bf934-b0a0-44b2-bea2-e8575404d36d">IMFVideoMixerBitmap::UpdateAlphaBitmapParameters</a> method.


### -field MFVideoAlphaBitmap_SrcColorKey

If this flag is set, the <b>clrSrcKey</b> member of the <a href="https://msdn.microsoft.com/3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce">MFVideoAlphaBitmapParams</a> structure specifies a color key for alpha-blending. If this flag is absent, the <b>clrSrcKey</b> member is ignored.

This flag is not valid if you are alpha-blending a Direct3D surface with per-pixel alpha (D3DFMT_A8R8G8B8). When the DirectDraw surface has per-pixel alpha, the pixel alpha values are used for the alpha-blending operation.


### -field MFVideoAlphaBitmap_SrcRect

Update the source rectangle.

This flag applies to the <a href="https://msdn.microsoft.com/369bf934-b0a0-44b2-bea2-e8575404d36d">UpdateAlphaBitmapParameters</a> method. If this flag is set, the <b>rcSrc</b> member of the <a href="https://msdn.microsoft.com/3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce">MFVideoAlphaBitmapParams</a> structure updates the source rectangle. If this flag is absent, the <b>rcSrc</b> member is ignored. By setting this flag, you can animate the image by selecting different portions of the bitmap.

This flag does not apply to the <a href="https://msdn.microsoft.com/a70e6734-bf49-4dea-8bf6-917b8465cc78">SetAlphaBitmap</a> method.


### -field MFVideoAlphaBitmap_DestRect

If this flag is set, the <b>nrcDest</b> member of the <a href="https://msdn.microsoft.com/3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce">MFVideoAlphaBitmapParams</a> structure specifies a normalized rectangle for scaling the bitmap. If this flag is absent, the <b>nrcDest</b> member is ignored.


### -field MFVideoAlphaBitmap_FilterMode

If this flag is set, the <b>dwFilterMode</b> member of the <a href="https://msdn.microsoft.com/3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce">MFVideoAlphaBitmapParams</a> structure specifies a Direct3D filtering mode. If this flag is absent, the <b>dwFilterMode</b> member is ignored.


### -field MFVideoAlphaBitmap_Alpha

If this flag is set, the <b>fAlpha</b> member of the <a href="https://msdn.microsoft.com/3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce">MFVideoAlphaBitmapParams</a> structure specifies an alpha value to apply to the entire image. If this flag is absent, the <b>fAlpha</b> member is ignored.


### -field MFVideoAlphaBitmap_BitMask

Bitmask to validate flag values. This value is not a valid flag.


## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

