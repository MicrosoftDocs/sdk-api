---
UID: NS:d3d11.D3D11_VIDEO_DECODER_DESC
title: D3D11_VIDEO_DECODER_DESC (d3d11.h)

description: Describes a video stream for a Microsoft Direct3D 11 video decoder or video processor.
old-location: mf\d3d11_video_decoder_desc.htm
tech.root: medfound
ms.assetid: 668D994C-B875-4666-B940-1052A6DE6AA1

ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_DECODER_DESC, D3D11_VIDEO_DECODER_DESC structure [Media Foundation], d3d11/D3D11_VIDEO_DECODER_DESC, mf.d3d11_video_decoder_desc
ms.topic: struct
f1_keywords: 
 - "d3d11/D3D11_VIDEO_DECODER_DESC"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_DECODER_DESC
targetos: Windows
req.typenames: D3D11_VIDEO_DECODER_DESC
req.redist: 
ms.custom: 19H1
---

# D3D11_VIDEO_DECODER_DESC structure


## -description


Describes a video stream for a Microsoft Direct3D 11 video decoder or video processor. 




## -struct-fields




### -field Guid

The decoding profile. To get the list of profiles supported by the device, call the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile">ID3D11VideoDevice::GetVideoDecoderProfile</a> method.


### -field SampleWidth

The width of the video frame, in pixels. 




### -field SampleHeight

The height of the video frame, in pixels. 




### -field OutputFormat

The output surface format, specified as a <a href="https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> value.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>
 

 

