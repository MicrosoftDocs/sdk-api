---
UID: NF:d3d11.ID3D11VideoDevice.GetVideoDecoderConfig
title: ID3D11VideoDevice::GetVideoDecoderConfig (d3d11.h)
description: Gets a decoder configuration that is supported by the driver.
helpviewer_keywords: ["GetVideoDecoderConfig","GetVideoDecoderConfig method [Media Foundation]","GetVideoDecoderConfig method [Media Foundation]","ID3D11VideoDevice interface","ID3D11VideoDevice interface [Media Foundation]","GetVideoDecoderConfig method","ID3D11VideoDevice.GetVideoDecoderConfig","ID3D11VideoDevice::GetVideoDecoderConfig","d3d11/ID3D11VideoDevice::GetVideoDecoderConfig","mf.id3d11videodevice_getvideodecoderconfig"]
old-location: mf\id3d11videodevice_getvideodecoderconfig.htm
tech.root: mf
ms.assetid: EC3B23BE-0A28-41E6-A515-7801C9E0A4D9
ms.date: 12/05/2018
ms.keywords: GetVideoDecoderConfig, GetVideoDecoderConfig method [Media Foundation], GetVideoDecoderConfig method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],GetVideoDecoderConfig method, ID3D11VideoDevice.GetVideoDecoderConfig, ID3D11VideoDevice::GetVideoDecoderConfig, d3d11/ID3D11VideoDevice::GetVideoDecoderConfig, mf.id3d11videodevice_getvideodecoderconfig
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
 - ID3D11VideoDevice::GetVideoDecoderConfig
 - d3d11/ID3D11VideoDevice::GetVideoDecoderConfig
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
 - ID3D11VideoDevice.GetVideoDecoderConfig
---

# ID3D11VideoDevice::GetVideoDecoderConfig


## -description

Gets a decoder configuration that is supported by the driver.

## -parameters

### -param pDesc [in]

A pointer to a  <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc">D3D11_VIDEO_DECODER_DESC</a> structure that describes the video stream.

### -param Index [in]

The zero-based index of the decoder configuration. To get the number of configurations that the driver supports, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount">ID3D11VideoDevice::GetVideoDecoderConfigCount</a>.

### -param pConfig [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config">D3D11_VIDEO_DECODER_CONFIG</a> structure. The method fills in the structure with the decoder configuration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>