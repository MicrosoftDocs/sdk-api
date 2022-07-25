---
UID: NN:dxva2api.IDirectXVideoDecoderService
title: IDirectXVideoDecoderService (dxva2api.h)
description: Provides access to DirectX Video Acceleration (DXVA) decoder services.
helpviewer_keywords: ["IDirectXVideoDecoderService","IDirectXVideoDecoderService interface [Media Foundation]","IDirectXVideoDecoderService interface [Media Foundation]","described","dxva2api/IDirectXVideoDecoderService","eeb62178-b54d-45d3-a584-75865f0662fa","mf.idirectxvideodecoderservice"]
old-location: mf\idirectxvideodecoderservice.htm
tech.root: mf
ms.assetid: eeb62178-b54d-45d3-a584-75865f0662fa
ms.date: 12/05/2018
ms.keywords: IDirectXVideoDecoderService, IDirectXVideoDecoderService interface [Media Foundation], IDirectXVideoDecoderService interface [Media Foundation],described, dxva2api/IDirectXVideoDecoderService, eeb62178-b54d-45d3-a584-75865f0662fa, mf.idirectxvideodecoderservice
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IDirectXVideoDecoderService
 - dxva2api/IDirectXVideoDecoderService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoDecoderService
---

# IDirectXVideoDecoderService interface


## -description

Provides access to DirectX Video Acceleration (DXVA) decoder services. Use this interface to query which hardware-accelerated decoding operations are available and to create DXVA video decoder devices. 

To get a pointer to this interface, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice">IDirect3DDeviceManager9::GetVideoService</a> or <a href="/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice">DXVA2CreateVideoService</a> with the interface identifier IID_IDirectXVideoDecoderService.

## -inheritance

The <b>IDirectXVideoDecoderService</b> interface inherits from <a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice">IDirectXVideoAccelerationService</a>. <b>IDirectXVideoDecoderService</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice">IDirectXVideoAccelerationService</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
