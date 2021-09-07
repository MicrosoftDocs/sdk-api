---
UID: NF:d3d11.ID3D11VideoDecoder.GetCreationParameters
title: ID3D11VideoDecoder::GetCreationParameters (d3d11.h)
description: Gets the parameters that were used to create the decoder.
helpviewer_keywords: ["GetCreationParameters","GetCreationParameters method [Media Foundation]","GetCreationParameters method [Media Foundation]","ID3D11VideoDecoder interface","ID3D11VideoDecoder interface [Media Foundation]","GetCreationParameters method","ID3D11VideoDecoder.GetCreationParameters","ID3D11VideoDecoder::GetCreationParameters","d3d11/ID3D11VideoDecoder::GetCreationParameters","mf.id3d11videodecoder_getcreationparameters"]
old-location: mf\id3d11videodecoder_getcreationparameters.htm
tech.root: mf
ms.assetid: 6F104317-19C2-4FCB-8CA7-34FD0C237822
ms.date: 12/05/2018
ms.keywords: GetCreationParameters, GetCreationParameters method [Media Foundation], GetCreationParameters method [Media Foundation],ID3D11VideoDecoder interface, ID3D11VideoDecoder interface [Media Foundation],GetCreationParameters method, ID3D11VideoDecoder.GetCreationParameters, ID3D11VideoDecoder::GetCreationParameters, d3d11/ID3D11VideoDecoder::GetCreationParameters, mf.id3d11videodecoder_getcreationparameters
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
 - ID3D11VideoDecoder::GetCreationParameters
 - d3d11/ID3D11VideoDecoder::GetCreationParameters
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
 - ID3D11VideoDecoder.GetCreationParameters
---

# ID3D11VideoDecoder::GetCreationParameters


## -description

Gets the parameters that were used to create the decoder.

## -parameters

### -param pVideoDesc [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc">D3D11_VIDEO_DECODER_DESC</a> structure that receives a description of the video stream.

### -param pConfig [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config">D3D11_VIDEO_DECODER_CONFIG</a> structure that receives the decoder configuration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a>