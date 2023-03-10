---
UID: NS:d3d11.D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
title: D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC (d3d11.h)
description: Describes a video decoder output view.
helpviewer_keywords: ["D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC","D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC structure [Media Foundation]","d3d11/D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC","mf.d3d11_video_decoder_output_view_desc"]
old-location: mf\d3d11_video_decoder_output_view_desc.htm
tech.root: mf
ms.assetid: 0A0C29C5-C3A3-43E7-86DA-1849AC276060
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC, D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC structure [Media Foundation], d3d11/D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC, mf.d3d11_video_decoder_output_view_desc
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
req.typenames: D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
 - d3d11/D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
---

# D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC structure


## -description

Describes a video decoder output view.

## -struct-fields

### -field DecodeProfile

The decoding profile. To get the list of profiles supported by the device, call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile">ID3D11VideoDevice::GetVideoDecoderProfile</a> method.

### -field ViewDimension

The resource type of the view, specified as a member of the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_vdov_dimension">D3D11_VDOV_DIMENSION</a> enumeration.

### -field Texture2D

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_vdov">D3D11_TEX2D_VDOV</a> structure that identifies the texture resource for the output view.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview">ID3D11VideoDevice::CreateVideoDecoderOutputView</a>