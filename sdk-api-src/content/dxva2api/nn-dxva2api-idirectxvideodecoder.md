---
UID: NN:dxva2api.IDirectXVideoDecoder
title: IDirectXVideoDecoder (dxva2api.h)
description: Represents a DirectX Video Acceleration (DXVA) video decoder device.
helpviewer_keywords: ["116c19a3-39be-4f96-969f-f3d62ed33a70","IDirectXVideoDecoder","IDirectXVideoDecoder interface [Media Foundation]","IDirectXVideoDecoder interface [Media Foundation]","described","dxva2api/IDirectXVideoDecoder","mf.idirectxvideodecoder"]
old-location: mf\idirectxvideodecoder.htm
tech.root: mf
ms.assetid: 116c19a3-39be-4f96-969f-f3d62ed33a70
ms.date: 12/05/2018
ms.keywords: 116c19a3-39be-4f96-969f-f3d62ed33a70, IDirectXVideoDecoder, IDirectXVideoDecoder interface [Media Foundation], IDirectXVideoDecoder interface [Media Foundation],described, dxva2api/IDirectXVideoDecoder, mf.idirectxvideodecoder
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
 - IDirectXVideoDecoder
 - dxva2api/IDirectXVideoDecoder
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
 - IDirectXVideoDecoder
---

# IDirectXVideoDecoder interface


## -description

Represents a DirectX Video Acceleration (DXVA) video decoder device.

 To get a pointer to this interface, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder">IDirectXVideoDecoderService::CreateVideoDecoder</a>.

## -inheritance

The <b>IDirectXVideoDecoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectXVideoDecoder</b> also has these types of members:

## -remarks

The <b>IDirectXVideoDecoder</b> methods make calls to the Direct3D device. Therefore, the <b>D3DCREATE</b> flags that you specify  when creating the device can affect the behavior of this interface. For example, if you specify the <b>D3DCREATE_MULTITHREADED</b> flag, the Direct3D global critical section will be held during decode operations.

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
