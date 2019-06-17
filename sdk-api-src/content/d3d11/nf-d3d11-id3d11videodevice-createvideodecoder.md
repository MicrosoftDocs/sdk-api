---
UID: NF:d3d11.ID3D11VideoDevice.CreateVideoDecoder
title: ID3D11VideoDevice::CreateVideoDecoder (d3d11.h)
author: windows-sdk-content
description: Creates a video decoder device for Microsoft Direct3D 11.
old-location: mf\id3d11videodevice_createvideodecoder.htm
tech.root: medfound
ms.assetid: 7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateVideoDecoder, CreateVideoDecoder method [Media Foundation], CreateVideoDecoder method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateVideoDecoder method, ID3D11VideoDevice.CreateVideoDecoder, ID3D11VideoDevice::CreateVideoDecoder, d3d11/ID3D11VideoDevice::CreateVideoDecoder, mf.id3d11videodevice_createvideodecoder
ms.topic: method
f1_keywords: ["d3d11/ID3D11VideoDevice.CreateVideoDecoder"]
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
 - ID3D11VideoDevice.CreateVideoDecoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoDevice::CreateVideoDecoder


## -description


Creates a video decoder device for Microsoft Direct3D 11.


## -parameters




### -param pVideoDesc [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc">D3D11_VIDEO_DECODER_DESC</a> structure that describes the video stream and the decoder profile.


### -param pConfig [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config">D3D11_VIDEO_DECODER_CONFIG</a> structure that specifies the decoder configuration.


### -param ppDecoder [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method allocates the necessary decoder buffers. 

The <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate">ID3D11DeviceContext::ClearState</a> method does not affect the internal state of the video decoder.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>
 

 

