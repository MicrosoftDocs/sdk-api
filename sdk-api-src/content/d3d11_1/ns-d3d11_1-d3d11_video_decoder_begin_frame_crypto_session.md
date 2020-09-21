---
UID: NS:d3d11_1.D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION
title: D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION (d3d11_1.h)
description: Provides data to the ID3D11VideoContext::DecoderBeginFrame method.
helpviewer_keywords: ["D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION","D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION structure [Media Foundation]","d3d11_1/D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION","mf.d3d11_video_decoder_begin_frame_crypto_session"]
old-location: mf\d3d11_video_decoder_begin_frame_crypto_session.htm
tech.root: mf
ms.assetid: 7A4E0B99-90EE-4669-813E-5A3CD58D24A7
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION, D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION structure [Media Foundation], d3d11_1/D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION, mf.d3d11_video_decoder_begin_frame_crypto_session
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
req.typenames: D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION
 - d3d11_1/D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_1.h
api_name:
 - D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION
---

## -description

Provides data to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe">ID3D11VideoContext::DecoderBeginFrame</a> method.

## -struct-fields

### -field pCryptoSession

A pointer to the ID3D11CryptoSession interface.  To get this pointer, call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession">ID3D11VideoDevice1::CreateCryptoSession</a>.

### -field BlobSize

The size of the memory buffer referenced by the <i>pBlob</i> member.

### -field pBlob

The definition of this buffer is dependent on the implementation of the secure execution environment. It could contain a sealed key blob or any other per-key data that the secure execution environment needs to pass to the decode API.

The definition of this buffer is dependent on the implementation of the secure environment. It may contain data specific to the current frame.

### -field pKeyInfoId

A pointer to a GUID identifying the hardware key.

### -field PrivateDataSize

The size of the memory buffer referenced by the <i>pPrivateData</i> member.

### -field pPrivateData

## -remarks

This structure is passed in the <i>pContentKey</i> parameter of the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe">ID3D11VideoContext::DecoderBeginFrame</a> function when <a href="/windows/desktop/medfound/direct3d-11-video-guids">D3D11_DECODER_ENCRYPTION_HW_CENC</a>  is specified in the <b>guidConfigBitstreamEncryption</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config">D3D11_VIDEO_DECODER_CONFIG</a> structure when creating the video decoder interface.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>