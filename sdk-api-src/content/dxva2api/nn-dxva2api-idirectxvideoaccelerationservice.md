---
UID: NN:dxva2api.IDirectXVideoAccelerationService
title: IDirectXVideoAccelerationService (dxva2api.h)
description: Provides DirectX Video Acceleration (DXVA) services from a Direct3D device.
helpviewer_keywords: ["50a2d8f7-d7c9-4d50-88cc-f6c8562fbb17","IDirectXVideoAccelerationService","IDirectXVideoAccelerationService interface [Media Foundation]","IDirectXVideoAccelerationService interface [Media Foundation]","described","dxva2api/IDirectXVideoAccelerationService","mf.idirectxvideoaccelerationservice"]
old-location: mf\idirectxvideoaccelerationservice.htm
tech.root: mf
ms.assetid: 50a2d8f7-d7c9-4d50-88cc-f6c8562fbb17
ms.date: 12/05/2018
ms.keywords: 50a2d8f7-d7c9-4d50-88cc-f6c8562fbb17, IDirectXVideoAccelerationService, IDirectXVideoAccelerationService interface [Media Foundation], IDirectXVideoAccelerationService interface [Media Foundation],described, dxva2api/IDirectXVideoAccelerationService, mf.idirectxvideoaccelerationservice
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
 - IDirectXVideoAccelerationService
 - dxva2api/IDirectXVideoAccelerationService
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
 - IDirectXVideoAccelerationService
---

# IDirectXVideoAccelerationService interface


## -description

Provides DirectX Video Acceleration (DXVA) services from a Direct3D device. To get a pointer to this interface, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice">IDirect3DDeviceManager9::GetVideoService</a> or <a href="/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice">DXVA2CreateVideoService</a>.

## -inheritance

The <b>IDirectXVideoAccelerationService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectXVideoAccelerationService</b> also has these types of members:

## -remarks

This is the base interface for DXVA services. The Direct3D device can support any of the following DXVA services, which derive from <b>IDirectXVideoAccelerationService</b>:

<ul>
<li>Video decoding: <a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice">IDirectXVideoDecoderService</a>
</li>
<li>Video processing: <a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice">IDirectXVideoProcessorService</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
