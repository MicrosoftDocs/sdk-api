---
UID: NF:dxva2api.IDirectXVideoDecoderService.GetDecoderConfigurations
title: IDirectXVideoDecoderService::GetDecoderConfigurations (dxva2api.h)
description: Gets the configurations that are available for a decoder device.
helpviewer_keywords: ["7d2c24f3-9066-4e8b-aad6-98b7245088a5","GetDecoderConfigurations","GetDecoderConfigurations method [Media Foundation]","GetDecoderConfigurations method [Media Foundation]","IDirectXVideoDecoderService interface","IDirectXVideoDecoderService interface [Media Foundation]","GetDecoderConfigurations method","IDirectXVideoDecoderService.GetDecoderConfigurations","IDirectXVideoDecoderService::GetDecoderConfigurations","dxva2api/IDirectXVideoDecoderService::GetDecoderConfigurations","mf.idirectxvideodecoderservice_getdecoderconfigurations"]
old-location: mf\idirectxvideodecoderservice_getdecoderconfigurations.htm
tech.root: mf
ms.assetid: 7d2c24f3-9066-4e8b-aad6-98b7245088a5
ms.date: 12/05/2018
ms.keywords: 7d2c24f3-9066-4e8b-aad6-98b7245088a5, GetDecoderConfigurations, GetDecoderConfigurations method [Media Foundation], GetDecoderConfigurations method [Media Foundation],IDirectXVideoDecoderService interface, IDirectXVideoDecoderService interface [Media Foundation],GetDecoderConfigurations method, IDirectXVideoDecoderService.GetDecoderConfigurations, IDirectXVideoDecoderService::GetDecoderConfigurations, dxva2api/IDirectXVideoDecoderService::GetDecoderConfigurations, mf.idirectxvideodecoderservice_getdecoderconfigurations
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
 - IDirectXVideoDecoderService::GetDecoderConfigurations
 - dxva2api/IDirectXVideoDecoderService::GetDecoderConfigurations
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
 - IDirectXVideoDecoderService.GetDecoderConfigurations
---

# IDirectXVideoDecoderService::GetDecoderConfigurations


## -description

Gets the configurations that are available for a decoder device.

## -parameters

### -param Guid [in]

A GUID that identifies the decoder device. To get the available device GUIDs, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids">IDirectXVideoDecoderService::GetDecoderDeviceGuids</a>.

### -param pVideoDesc [in]

A pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc">DXVA2_VideoDesc</a> structure that describes the video content.

### -param pReserved [in]

Reserved. Set to <b>NULL</b>.

### -param pCount [out]

Receives the number of configurations.

### -param ppConfigs [out]

Receives an array of <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode">DXVA2_ConfigPictureDecode</a> structures. The size of the array is retrieved in the <i>pCount</i> parameter. The caller must free the memory for the array by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. This parameter can be <b>NULL</b> if you simply want the number of configurations (returned in <i>pCount</i>) but not the GUIDs.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode">DXVA2_ConfigPictureDecode</a>



<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice">IDirectXVideoDecoderService</a>