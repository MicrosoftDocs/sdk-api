---
UID: NF:dxva2api.IDirectXVideoDecoderService.CreateVideoDecoder
title: IDirectXVideoDecoderService::CreateVideoDecoder (dxva2api.h)
description: Creates a video decoder device.
helpviewer_keywords: ["2a799411-e8d5-4ab8-b52f-7198af9a4f2b","CreateVideoDecoder","CreateVideoDecoder method [Media Foundation]","CreateVideoDecoder method [Media Foundation]","IDirectXVideoDecoderService interface","IDirectXVideoDecoderService interface [Media Foundation]","CreateVideoDecoder method","IDirectXVideoDecoderService.CreateVideoDecoder","IDirectXVideoDecoderService::CreateVideoDecoder","dxva2api/IDirectXVideoDecoderService::CreateVideoDecoder","mf.idirectxvideodecoderservice_createvideodecoder"]
old-location: mf\idirectxvideodecoderservice_createvideodecoder.htm
tech.root: mf
ms.assetid: 2a799411-e8d5-4ab8-b52f-7198af9a4f2b
ms.date: 12/05/2018
ms.keywords: 2a799411-e8d5-4ab8-b52f-7198af9a4f2b, CreateVideoDecoder, CreateVideoDecoder method [Media Foundation], CreateVideoDecoder method [Media Foundation],IDirectXVideoDecoderService interface, IDirectXVideoDecoderService interface [Media Foundation],CreateVideoDecoder method, IDirectXVideoDecoderService.CreateVideoDecoder, IDirectXVideoDecoderService::CreateVideoDecoder, dxva2api/IDirectXVideoDecoderService::CreateVideoDecoder, mf.idirectxvideodecoderservice_createvideodecoder
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
 - IDirectXVideoDecoderService::CreateVideoDecoder
 - dxva2api/IDirectXVideoDecoderService::CreateVideoDecoder
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
 - IDirectXVideoDecoderService.CreateVideoDecoder
---

# IDirectXVideoDecoderService::CreateVideoDecoder


## -description

Creates a video decoder device.

## -parameters

### -param Guid [in]

GUID that specifies the decoder device to create. To get the available device GUIDs, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids">IDirectXVideoDecoderService::GetDecoderDeviceGuids</a>.

### -param pVideoDesc [in]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc">DXVA2_VideoDesc</a> structure that describes the video content.

### -param pConfig [in]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode">DXVA2_ConfigPictureDecode</a> structure that specifies the decoder configuration.

### -param ppDecoderRenderTargets [in]

Pointer to an array of <b>IDirect3DSurface9</b> pointers containing pointers to the decoder render targets. To create these surfaces, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface">IDirectXVideoAccelerationService::CreateSurface</a>. Specify DXVA2_VideoDecoderRenderTarget for the <i>DxvaType</i> parameter.

### -param NumRenderTargets [in]

Size of the <i>ppDecoderRenderTargets</i> array. This value cannot be zero.

### -param ppDecode [out]

Receives a pointer to the decoder's <a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder">IDirectXVideoDecoder</a> interface. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice">IDirectXVideoDecoderService</a>