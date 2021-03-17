---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamPalette
title: ID3D11VideoContext::VideoProcessorGetStreamPalette (d3d11.h)
description: Gets the color-palette entries for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetStreamPalette method","ID3D11VideoContext.VideoProcessorGetStreamPalette","ID3D11VideoContext::VideoProcessorGetStreamPalette","VideoProcessorGetStreamPalette","VideoProcessorGetStreamPalette method [Media Foundation]","VideoProcessorGetStreamPalette method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetStreamPalette","mf.id3d11videocontext_videoprocessorgetstreampalette"]
old-location: mf\id3d11videocontext_videoprocessorgetstreampalette.htm
tech.root: mf
ms.assetid: 009568EA-7230-42C0-B35F-AB0A1AF8EC2A
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamPalette method, ID3D11VideoContext.VideoProcessorGetStreamPalette, ID3D11VideoContext::VideoProcessorGetStreamPalette, VideoProcessorGetStreamPalette, VideoProcessorGetStreamPalette method [Media Foundation], VideoProcessorGetStreamPalette method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamPalette, mf.id3d11videocontext_videoprocessorgetstreampalette
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
 - ID3D11VideoContext::VideoProcessorGetStreamPalette
 - d3d11/ID3D11VideoContext::VideoProcessorGetStreamPalette
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
 - ID3D11VideoContext.VideoProcessorGetStreamPalette
---

# ID3D11VideoContext::VideoProcessorGetStreamPalette


## -description

Gets the color-palette entries for an input stream on the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param Count [in]

The number of entries in the <i>pEntries</i> array.

### -param pEntries [out]

A pointer to a <b>UINT</b> array allocated by the caller. The method fills the array with the palette entries. For RGB streams, the palette entries use the <b>DXGI_FORMAT_B8G8R8A8</b> representation. For YCbCr streams, the palette entries use the <b>DXGI_FORMAT_AYUV</b> representation.

## -remarks

This method applies only to input streams that have a palettized color format. Palettized formats with 4 bits per pixel (bpp) use 16 palette entries. Formats with 8 bpp use 256 entries.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>