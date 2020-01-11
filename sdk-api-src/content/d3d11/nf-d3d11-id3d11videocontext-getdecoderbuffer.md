---
UID: NF:d3d11.ID3D11VideoContext.GetDecoderBuffer
title: ID3D11VideoContext::GetDecoderBuffer (d3d11.h)
description: Gets a pointer to a decoder buffer.
old-location: mf\id3d11videocontext_getdecoderbuffer.htm
tech.root: medfound
ms.assetid: 6842D5D7-6165-4428-91BD-2234BE5332B8
ms.date: 12/05/2018
ms.keywords: GetDecoderBuffer, GetDecoderBuffer method [Media Foundation], GetDecoderBuffer method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],GetDecoderBuffer method, ID3D11VideoContext.GetDecoderBuffer, ID3D11VideoContext::GetDecoderBuffer, d3d11/ID3D11VideoContext::GetDecoderBuffer, mf.id3d11videocontext_getdecoderbuffer
f1_keywords:
- d3d11/ID3D11VideoContext.GetDecoderBuffer
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
- COM
api_location:
- d3d11.h
api_name:
- ID3D11VideoContext.GetDecoderBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::GetDecoderBuffer


## -description


Gets a pointer to a decoder buffer.


## -parameters




### -param pDecoder [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder">ID3D11VideoDevice::CreateVideoDecoder</a>.


### -param Type [in]

The type of buffer to retrieve, specified as a member of the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_decoder_buffer_type">D3D11_VIDEO_DECODER_BUFFER_TYPE</a> enumeration.


### -param pBufferSize [out]

Receives the size of the buffer, in bytes.




### -param ppBuffer [out]

Receives a pointer to the start of the memory buffer.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The graphics driver allocates the buffers that are used for decoding. This method locks the Microsoft Direct3Dsurface that contains the buffer. When you are done using the buffer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer">ID3D11VideoContext::ReleaseDecoderBuffer</a> to unlock the surface.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

