---
UID: NF:d3d11.ID3D11VideoContext.ReleaseDecoderBuffer
title: ID3D11VideoContext::ReleaseDecoderBuffer (d3d11.h)
description: Releases a buffer that was obtained by calling the ID3D11VideoContext::GetDecoderBuffer method.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","ReleaseDecoderBuffer method","ID3D11VideoContext.ReleaseDecoderBuffer","ID3D11VideoContext::ReleaseDecoderBuffer","ReleaseDecoderBuffer","ReleaseDecoderBuffer method [Media Foundation]","ReleaseDecoderBuffer method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::ReleaseDecoderBuffer","mf.id3d11videocontext_releasedecoderbuffer"]
old-location: mf\id3d11videocontext_releasedecoderbuffer.htm
tech.root: mf
ms.assetid: C7BD4CA6-706D-4C3A-AED1-EDF1C65E41E0
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],ReleaseDecoderBuffer method, ID3D11VideoContext.ReleaseDecoderBuffer, ID3D11VideoContext::ReleaseDecoderBuffer, ReleaseDecoderBuffer, ReleaseDecoderBuffer method [Media Foundation], ReleaseDecoderBuffer method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::ReleaseDecoderBuffer, mf.id3d11videocontext_releasedecoderbuffer
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
 - ID3D11VideoContext::ReleaseDecoderBuffer
 - d3d11/ID3D11VideoContext::ReleaseDecoderBuffer
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
 - ID3D11VideoContext.ReleaseDecoderBuffer
---

# ID3D11VideoContext::ReleaseDecoderBuffer


## -description

Releases a buffer that was obtained by calling the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer">ID3D11VideoContext::GetDecoderBuffer</a> method.

## -parameters

### -param pDecoder [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder">ID3D11VideoDevice::CreateVideoDecoder</a>.

### -param Type [in]

The type of buffer to release. Specify the same value that was used in the <i>Type</i> parameter of the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer">GetDecoderBuffer</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>