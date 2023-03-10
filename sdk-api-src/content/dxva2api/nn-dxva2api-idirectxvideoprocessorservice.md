---
UID: NN:dxva2api.IDirectXVideoProcessorService
title: IDirectXVideoProcessorService (dxva2api.h)
description: Provides access to DirectX Video Acceleration (DXVA) video processing services.
helpviewer_keywords: ["IDirectXVideoProcessorService","IDirectXVideoProcessorService interface [Media Foundation]","IDirectXVideoProcessorService interface [Media Foundation]","described","dxva2api/IDirectXVideoProcessorService","fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688","mf.idirectxvideoprocessorservice"]
old-location: mf\idirectxvideoprocessorservice.htm
tech.root: mf
ms.assetid: fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688
ms.date: 12/05/2018
ms.keywords: IDirectXVideoProcessorService, IDirectXVideoProcessorService interface [Media Foundation], IDirectXVideoProcessorService interface [Media Foundation],described, dxva2api/IDirectXVideoProcessorService, fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688, mf.idirectxvideoprocessorservice
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
 - IDirectXVideoProcessorService
 - dxva2api/IDirectXVideoProcessorService
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
 - IDirectXVideoProcessorService
---

# IDirectXVideoProcessorService interface


## -description

Provides access to DirectX Video Acceleration (DXVA) video processing services.

Use this interface to query which hardware-accelerated video processing operations are available and to create DXVA video processor devices. To obtain a pointer to this interface, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice">IDirect3DDeviceManager9::GetVideoService</a> or <a href="/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice">DXVA2CreateVideoService</a> with the interface identifier <b>IID_IDirectXVideoProcessorService</b>.

## -inheritance

The <b>IDirectXVideoProcessorService</b> interface inherits from <a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice">IDirectXVideoAccelerationService</a>. <b>IDirectXVideoProcessorService</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice">IDirectXVideoAccelerationService</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
