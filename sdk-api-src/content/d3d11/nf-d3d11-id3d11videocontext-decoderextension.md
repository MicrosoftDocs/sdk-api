---
UID: NF:d3d11.ID3D11VideoContext.DecoderExtension
title: ID3D11VideoContext::DecoderExtension (d3d11.h)
author: windows-sdk-content
description: Performs an extended function for decoding.
old-location: mf\id3d11videocontext_decoderextension.htm
tech.root: medfound
ms.assetid: B96FD793-C82A-4752-8F59-3CC9B86D1C2D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DecoderExtension, DecoderExtension method [Media Foundation], DecoderExtension method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],DecoderExtension method, ID3D11VideoContext.DecoderExtension, ID3D11VideoContext::DecoderExtension, d3d11/ID3D11VideoContext::DecoderExtension, mf.id3d11videocontext_decoderextension
ms.topic: method
f1_keywords: 
 - "d3d11/ID3D11VideoContext.DecoderExtension"
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ID3D11VideoContext.DecoderExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::DecoderExtension


## -description


Performs an extended function for decoding. This method enables extensions to the basic decoder functionality.


## -parameters




### -param pDecoder [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder">ID3D11VideoDevice::CreateVideoDecoder</a>.


### -param pExtensionData [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_extension">D3D11_VIDEO_DECODER_EXTENSION</a> structure that contains data for the function.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

