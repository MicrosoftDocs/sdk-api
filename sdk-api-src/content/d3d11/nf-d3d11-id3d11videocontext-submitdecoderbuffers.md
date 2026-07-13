---
UID: NF:d3d11.ID3D11VideoContext.SubmitDecoderBuffers
title: ID3D11VideoContext::SubmitDecoderBuffers (d3d11.h)
description: Submits one or more buffers for decoding. (ID3D11VideoContext.SubmitDecoderBuffers)
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","SubmitDecoderBuffers method","ID3D11VideoContext.SubmitDecoderBuffers","ID3D11VideoContext::SubmitDecoderBuffers","SubmitDecoderBuffers","SubmitDecoderBuffers method [Media Foundation]","SubmitDecoderBuffers method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::SubmitDecoderBuffers","mf.id3d11videocontext_submitdecoderbuffers"]
old-location: mf\id3d11videocontext_submitdecoderbuffers.htm
tech.root: mf
ms.assetid: 39010E57-FFF2-4793-B839-E336E8D2C1B2
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],SubmitDecoderBuffers method, ID3D11VideoContext.SubmitDecoderBuffers, ID3D11VideoContext::SubmitDecoderBuffers, SubmitDecoderBuffers, SubmitDecoderBuffers method [Media Foundation], SubmitDecoderBuffers method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::SubmitDecoderBuffers, mf.id3d11videocontext_submitdecoderbuffers
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
 - ID3D11VideoContext::SubmitDecoderBuffers
 - d3d11/ID3D11VideoContext::SubmitDecoderBuffers
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
 - ID3D11VideoContext.SubmitDecoderBuffers
---

# ID3D11VideoContext::SubmitDecoderBuffers


## -description

Submits one or more buffers for decoding.

## -parameters

### -param pDecoder [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface. To get this pointer, call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder">ID3D11VideoDevice::CreateVideoDecoder</a> method.

### -param NumBuffers [in]

The number of buffers submitted for decoding.

### -param pBufferDesc [in]

A pointer to an array of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_buffer_desc">D3D11_VIDEO_DECODER_BUFFER_DESC</a> structures. The <i>NumBuffers</i> parameter specifies the number of elements in the array. Each element in the array describes a compressed buffer for decoding.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function does not honor a D3D11 predicate that may have been set.

If the application uses <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_query">D3D11 queries</a>, this function may not be accounted for with <b>D3D11_QUERY_EVENT</b> and <b>D3D11_QUERY_TIMESTAMP</b> when using feature levels lower than 11.  <b>D3D11_QUERY_PIPELINE_STATISTICS</b> will not include this function for any feature level.

When using feature levels 9_x, all partially encrypted buffers must use the same EncryptedBlockInfo, and partial encryption cannot be turned off on a per frame basis.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
