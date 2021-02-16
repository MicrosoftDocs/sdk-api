---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamPalette
title: ID3D11VideoContext::VideoProcessorSetStreamPalette (d3d11.h)
description: Sets the color-palette entries for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamPalette method","ID3D11VideoContext.VideoProcessorSetStreamPalette","ID3D11VideoContext::VideoProcessorSetStreamPalette","VideoProcessorSetStreamPalette","VideoProcessorSetStreamPalette method [Media Foundation]","VideoProcessorSetStreamPalette method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamPalette","mf.id3d11videocontext_videoprocessorsetstreampalette"]
old-location: mf\id3d11videocontext_videoprocessorsetstreampalette.htm
tech.root: mf
ms.assetid: E2816D5F-0541-45B0-A90A-7C26530D064C
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamPalette method, ID3D11VideoContext.VideoProcessorSetStreamPalette, ID3D11VideoContext::VideoProcessorSetStreamPalette, VideoProcessorSetStreamPalette, VideoProcessorSetStreamPalette method [Media Foundation], VideoProcessorSetStreamPalette method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamPalette, mf.id3d11videocontext_videoprocessorsetstreampalette
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext::VideoProcessorSetStreamPalette
 - d3d11/ID3D11VideoContext::VideoProcessorSetStreamPalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorSetStreamPalette
---

# ID3D11VideoContext::VideoProcessorSetStreamPalette


## -description

Sets the color-palette entries for an input stream on the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param Count [in]

The number of elements in the <i>pEntries</i> array.

### -param pEntries [in]

A pointer to an array of palette entries. For RGB streams, the palette entries use the <b>DXGI_FORMAT_B8G8R8A8</b> representation. For YCbCr streams, the palette entries use the <b>DXGI_FORMAT_AYUV</b> representation. The caller allocates the array.

## -remarks

This method applies only to  input streams that have a palettized color format. Palettized formats with 4 bits per pixel (bpp) use the first 16 entries in the list. Formats with 8 bpp use the first 256 entries.

If a pixel has a palette index greater than the number of entries, the device treats the pixel as white with opaque alpha. For full-range RGB, this value is (255, 255, 255, 255); for YCbCr the value is (255, 235, 128, 128).

If the driver does not report the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_PALETTE</b> capability flag, every palette entry must have an alpha value of 0xFF (opaque). To query for this capability, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>