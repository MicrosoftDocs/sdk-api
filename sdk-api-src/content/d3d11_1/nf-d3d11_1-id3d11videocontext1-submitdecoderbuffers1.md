---
UID: NF:d3d11_1.ID3D11VideoContext1.SubmitDecoderBuffers1
title: ID3D11VideoContext1::SubmitDecoderBuffers1 (d3d11_1.h)
description: Submits one or more buffers for decoding. (ID3D11VideoContext1.SubmitDecoderBuffers1)
helpviewer_keywords: ["ID3D11VideoContext1 interface [Media Foundation]","SubmitDecoderBuffers1 method","ID3D11VideoContext1.SubmitDecoderBuffers1","ID3D11VideoContext1::SubmitDecoderBuffers1","SubmitDecoderBuffers1","SubmitDecoderBuffers1 method [Media Foundation]","SubmitDecoderBuffers1 method [Media Foundation]","ID3D11VideoContext1 interface","d3d11_1/ID3D11VideoContext1::SubmitDecoderBuffers1","mf.id3d11videocontext1_submitdecoderbuffers1"]
old-location: mf\id3d11videocontext1_submitdecoderbuffers1.htm
tech.root: mf
ms.assetid: 9E5FC926-71D7-4102-8952-EC0585B4A4FC
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],SubmitDecoderBuffers1 method, ID3D11VideoContext1.SubmitDecoderBuffers1, ID3D11VideoContext1::SubmitDecoderBuffers1, SubmitDecoderBuffers1, SubmitDecoderBuffers1 method [Media Foundation], SubmitDecoderBuffers1 method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::SubmitDecoderBuffers1, mf.id3d11videocontext1_submitdecoderbuffers1
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D11VideoContext1::SubmitDecoderBuffers1
 - d3d11_1/ID3D11VideoContext1::SubmitDecoderBuffers1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1.SubmitDecoderBuffers1
---

# ID3D11VideoContext1::SubmitDecoderBuffers1


## -description

Submits one or more buffers for decoding.

## -parameters

### -param pDecoder [in]

Type: <b>ID3D11VideoDecoder*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface. To get this pointer, call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder">ID3D11VideoDevice::CreateVideoDecoder</a> method.

### -param NumBuffers [in]

Type: <b>UINT</b>

The number of buffers submitted for decoding.

### -param pBufferDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_buffer_desc1">D3D11_VIDEO_DECODER_BUFFER_DESC1</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_buffer_desc1">D3D11_VIDEO_DECODER_BUFFER_DESC1</a> structures. The <i>NumBuffers</i> parameter specifies the number of elements in the array. Each element in the array describes a compressed buffer for decoding.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

This function does not honor any D3D11 predicate that may have been set.

<a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_data_pipeline_statistics">D3D11_QUERY_DATA_PIPELINE_STATISTICS</a> will not include this function for any feature level.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>
