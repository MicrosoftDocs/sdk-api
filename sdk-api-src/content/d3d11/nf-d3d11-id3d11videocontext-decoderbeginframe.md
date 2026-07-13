---
UID: NF:d3d11.ID3D11VideoContext.DecoderBeginFrame
title: ID3D11VideoContext::DecoderBeginFrame (d3d11.h)
description: Starts a decoding operation to decode a video frame.
helpviewer_keywords: ["DecoderBeginFrame","DecoderBeginFrame method [Media Foundation]","DecoderBeginFrame method [Media Foundation]","ID3D11VideoContext interface","ID3D11VideoContext interface [Media Foundation]","DecoderBeginFrame method","ID3D11VideoContext.DecoderBeginFrame","ID3D11VideoContext::DecoderBeginFrame","d3d11/ID3D11VideoContext::DecoderBeginFrame","mf.id3d11videocontext_decoderbeginframe"]
old-location: mf\id3d11videocontext_decoderbeginframe.htm
tech.root: mf
ms.assetid: 395B06D8-1BCF-44F2-9F69-A183C30E36B7
ms.date: 12/05/2018
ms.keywords: DecoderBeginFrame, DecoderBeginFrame method [Media Foundation], DecoderBeginFrame method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],DecoderBeginFrame method, ID3D11VideoContext.DecoderBeginFrame, ID3D11VideoContext::DecoderBeginFrame, d3d11/ID3D11VideoContext::DecoderBeginFrame, mf.id3d11videocontext_decoderbeginframe
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
 - ID3D11VideoContext::DecoderBeginFrame
 - d3d11/ID3D11VideoContext::DecoderBeginFrame
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
 - ID3D11VideoContext.DecoderBeginFrame
---

# ID3D11VideoContext::DecoderBeginFrame


## -description

Starts a decoding operation to decode a video frame.

## -parameters

### -param pDecoder [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder">ID3D11VideoDevice::CreateVideoDecoder</a>.

### -param pView [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview">ID3D11VideoDecoderOutputView</a> interface. This interface describes the resource that will receive the decoded frame. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview">ID3D11VideoDevice::CreateVideoDecoderOutputView</a>.

### -param ContentKeySize [in]

The size of the content key that is specified in <i>pContentKey</i>. If <i>pContentKey</i> is NULL, set <i>ContentKeySize</i> to zero.

### -param pContentKey [in]

An optional pointer to a content key that was used to encrypt the frame data. If no content key was used, set this parameter to <b>NULL</b>. If the caller provides a content key, the caller must use the session key to encrypt the content key.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.  <b>D3DERR_WASSTILLDRAWING</b> or <b>E_PENDING</b> is returned if the hardware is busy, in which case the decoder should try to make the call again.

## -remarks

After this method is called, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers">ID3D11VideoContext::SubmitDecoderBuffers</a> to perform decoding operations. When all decoding operations have been executed, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe">ID3D11VideoContext::DecoderEndFrame</a>.



Each call to <b>DecoderBeginFrame</b> must have a matching call to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe">DecoderEndFrame</a>. In most cases you cannot nest <b>DecoderBeginFrame</b> calls, but some codecs, such as  like VC-1, can have nested <b>DecoderBeginFrame</b> calls for special operations like post processing.

The following encryption scenarios are supported through the content key:

<ul>
<li>The decoder can choose to not encrypt every frame, for example  it may only encrypt the I frames and not encrypt the P/B frames.  In these scenario, the decoder will specify pContentKey = NULL and ContentKeySize = 0 for those frames that it does not encrypt.</li>
<li>The decoder can choose to encrypt the compressed buffers using the session key.  In this scenario, the decoder will specify a content key containing all zeros.</li>
<li>The decoder can choose to encrypt the compressed buffers using a separate content key.  In this scenario, the decoder will ECB encrypt the content key using the session key and pass the encrypted content key.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
