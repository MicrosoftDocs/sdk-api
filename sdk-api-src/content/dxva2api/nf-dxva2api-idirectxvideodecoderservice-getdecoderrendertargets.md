---
UID: NF:dxva2api.IDirectXVideoDecoderService.GetDecoderRenderTargets
title: IDirectXVideoDecoderService::GetDecoderRenderTargets (dxva2api.h)
description: Retrieves the supported render targets for a specified decoder device.
helpviewer_keywords: ["GetDecoderRenderTargets","GetDecoderRenderTargets method [Media Foundation]","GetDecoderRenderTargets method [Media Foundation]","IDirectXVideoDecoderService interface","IDirectXVideoDecoderService interface [Media Foundation]","GetDecoderRenderTargets method","IDirectXVideoDecoderService.GetDecoderRenderTargets","IDirectXVideoDecoderService::GetDecoderRenderTargets","cde04894-9042-4916-b195-60d84d0f87ec","dxva2api/IDirectXVideoDecoderService::GetDecoderRenderTargets","mf.idirectxvideodecoderservice_getdecoderrendertargets"]
old-location: mf\idirectxvideodecoderservice_getdecoderrendertargets.htm
tech.root: mf
ms.assetid: cde04894-9042-4916-b195-60d84d0f87ec
ms.date: 12/05/2018
ms.keywords: GetDecoderRenderTargets, GetDecoderRenderTargets method [Media Foundation], GetDecoderRenderTargets method [Media Foundation],IDirectXVideoDecoderService interface, IDirectXVideoDecoderService interface [Media Foundation],GetDecoderRenderTargets method, IDirectXVideoDecoderService.GetDecoderRenderTargets, IDirectXVideoDecoderService::GetDecoderRenderTargets, cde04894-9042-4916-b195-60d84d0f87ec, dxva2api/IDirectXVideoDecoderService::GetDecoderRenderTargets, mf.idirectxvideodecoderservice_getdecoderrendertargets
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
 - IDirectXVideoDecoderService::GetDecoderRenderTargets
 - dxva2api/IDirectXVideoDecoderService::GetDecoderRenderTargets
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
 - IDirectXVideoDecoderService.GetDecoderRenderTargets
---

# IDirectXVideoDecoderService::GetDecoderRenderTargets


## -description

Retrieves the supported render targets for a specified decoder device.

## -parameters

### -param Guid [in]

GUID that identifies the decoder device. To get the available device GUIDs, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids">IDirectXVideoDecoderService::GetDecoderDeviceGuids</a>.

### -param pCount [out]

Receives the number of formats.

### -param pFormats [out]

Receives an array of formats, specified as <b>D3DFORMAT</b> values. The size of the array is retrieved in the <i>pCount</i> parameter. The method allocates the memory for the array. The caller must free the memory by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

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