---
UID: NF:d3d11.ID3D11VideoContext.DecoderEndFrame
title: ID3D11VideoContext::DecoderEndFrame (d3d11.h)
description: Signals the end of a decoding operation.
helpviewer_keywords: ["DecoderEndFrame","DecoderEndFrame method [Media Foundation]","DecoderEndFrame method [Media Foundation]","ID3D11VideoContext interface","ID3D11VideoContext interface [Media Foundation]","DecoderEndFrame method","ID3D11VideoContext.DecoderEndFrame","ID3D11VideoContext::DecoderEndFrame","d3d11/ID3D11VideoContext::DecoderEndFrame","mf.id3d11videocontext_decoderendframe"]
old-location: mf\id3d11videocontext_decoderendframe.htm
tech.root: mf
ms.assetid: 3596B70C-4BED-49C4-A0E4-8702DA219B01
ms.date: 12/05/2018
ms.keywords: DecoderEndFrame, DecoderEndFrame method [Media Foundation], DecoderEndFrame method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],DecoderEndFrame method, ID3D11VideoContext.DecoderEndFrame, ID3D11VideoContext::DecoderEndFrame, d3d11/ID3D11VideoContext::DecoderEndFrame, mf.id3d11videocontext_decoderendframe
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
 - ID3D11VideoContext::DecoderEndFrame
 - d3d11/ID3D11VideoContext::DecoderEndFrame
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
 - ID3D11VideoContext.DecoderEndFrame
---

# ID3D11VideoContext::DecoderEndFrame


## -description

Signals the end of a decoding operation.

## -parameters

### -param pDecoder [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder">ID3D11VideoDevice::CreateVideoDecoder</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe">ID3D11VideoContext::DecoderBeginFrame</a>