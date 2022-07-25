---
UID: NF:d3d11.ID3D11VideoDevice.GetVideoDecoderConfigCount
title: ID3D11VideoDevice::GetVideoDecoderConfigCount (d3d11.h)
description: Gets the number of decoder configurations that the driver supports for a specified video description.
helpviewer_keywords: ["GetVideoDecoderConfigCount","GetVideoDecoderConfigCount method [Media Foundation]","GetVideoDecoderConfigCount method [Media Foundation]","ID3D11VideoDevice interface","ID3D11VideoDevice interface [Media Foundation]","GetVideoDecoderConfigCount method","ID3D11VideoDevice.GetVideoDecoderConfigCount","ID3D11VideoDevice::GetVideoDecoderConfigCount","d3d11/ID3D11VideoDevice::GetVideoDecoderConfigCount","mf.id3d11videodevice_getvideodecoderconfigcount"]
old-location: mf\id3d11videodevice_getvideodecoderconfigcount.htm
tech.root: mf
ms.assetid: C6650546-2F6D-4B91-888D-3A5A1AE86DCB
ms.date: 12/05/2018
ms.keywords: GetVideoDecoderConfigCount, GetVideoDecoderConfigCount method [Media Foundation], GetVideoDecoderConfigCount method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],GetVideoDecoderConfigCount method, ID3D11VideoDevice.GetVideoDecoderConfigCount, ID3D11VideoDevice::GetVideoDecoderConfigCount, d3d11/ID3D11VideoDevice::GetVideoDecoderConfigCount, mf.id3d11videodevice_getvideodecoderconfigcount
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
 - ID3D11VideoDevice::GetVideoDecoderConfigCount
 - d3d11/ID3D11VideoDevice::GetVideoDecoderConfigCount
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
 - ID3D11VideoDevice.GetVideoDecoderConfigCount
---

# ID3D11VideoDevice::GetVideoDecoderConfigCount


## -description

Gets the number of decoder configurations that the driver supports for a specified video description.

## -parameters

### -param pDesc [in]

A pointer to a  <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc">D3D11_VIDEO_DECODER_DESC</a> structure that describes the video stream.

### -param pCount [out]

Receives the number of decoder configurations.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To enumerate the decoder configurations, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig">ID3D11VideoDevice::GetVideoDecoderConfig</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>