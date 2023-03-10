---
UID: NF:mfapi.MFInitVideoFormat_RGB
title: MFInitVideoFormat_RGB function (mfapi.h)
description: Initializes an MFVIDEOFORMAT structure for an uncompressed RGB video format.
helpviewer_keywords: ["4c437f26-6fe1-477d-9955-bc900215aa59","MFInitVideoFormat_RGB","MFInitVideoFormat_RGB function [Media Foundation]","mf.mfinitvideoformat_rgb","mfapi/MFInitVideoFormat_RGB"]
old-location: mf\mfinitvideoformat_rgb.htm
tech.root: mf
ms.assetid: 4c437f26-6fe1-477d-9955-bc900215aa59
ms.date: 12/05/2018
ms.keywords: 4c437f26-6fe1-477d-9955-bc900215aa59, MFInitVideoFormat_RGB, MFInitVideoFormat_RGB function [Media Foundation], mf.mfinitvideoformat_rgb, mfapi/MFInitVideoFormat_RGB
req.header: mfapi.h
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
req.lib: Evr.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFInitVideoFormat_RGB
 - mfapi/MFInitVideoFormat_RGB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFInitVideoFormat_RGB
---

# MFInitVideoFormat_RGB function


## -description

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>.]

Initializes an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure for an uncompressed RGB video format.

## -parameters

### -param pVideoFormat [in]

A pointer to an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure. The functions fills in the structure members with the format information.

### -param dwWidth [in]

The width of the video, in pixels.

### -param dwHeight [in]

The height of the video, in pixels.

### -param D3Dfmt [in]

A <b>D3DFORMAT</b> value that specifies the RGB format.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function fills in some reasonable default values for the specified RGB format.
      

Developers are encouraged to use media type attributes instead of using the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure. See <a href="/windows/desktop/medfound/media-type-attributes">Media Type Attributes</a>.
      

In general, you should avoid calling this function. If you know all of the format details, you can fill in the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure without this function. If you do not know all of the format details, attributes are preferable to using the <b>MFVIDEOFORMAT</b> structure.
      

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>



<a href="/windows/desktop/medfound/uncompressed-video-media-types">Uncompressed Video Media Types</a>



<a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>