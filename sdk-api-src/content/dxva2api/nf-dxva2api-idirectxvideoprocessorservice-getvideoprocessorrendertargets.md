---
UID: NF:dxva2api.IDirectXVideoProcessorService.GetVideoProcessorRenderTargets
title: IDirectXVideoProcessorService::GetVideoProcessorRenderTargets (dxva2api.h)
description: Gets the render target formats that a video processor device supports. The list may include RGB and YUV formats.
helpviewer_keywords: ["GetVideoProcessorRenderTargets","GetVideoProcessorRenderTargets method [Media Foundation]","GetVideoProcessorRenderTargets method [Media Foundation]","IDirectXVideoProcessorService interface","IDirectXVideoProcessorService interface [Media Foundation]","GetVideoProcessorRenderTargets method","IDirectXVideoProcessorService.GetVideoProcessorRenderTargets","IDirectXVideoProcessorService::GetVideoProcessorRenderTargets","aecbba1e-309c-4668-9e17-d59710d86151","dxva2api/IDirectXVideoProcessorService::GetVideoProcessorRenderTargets","mf.idirectxvideoprocessorservice_getvideoprocessorrendertargets"]
old-location: mf\idirectxvideoprocessorservice_getvideoprocessorrendertargets.htm
tech.root: mf
ms.assetid: aecbba1e-309c-4668-9e17-d59710d86151
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorRenderTargets, GetVideoProcessorRenderTargets method [Media Foundation], GetVideoProcessorRenderTargets method [Media Foundation],IDirectXVideoProcessorService interface, IDirectXVideoProcessorService interface [Media Foundation],GetVideoProcessorRenderTargets method, IDirectXVideoProcessorService.GetVideoProcessorRenderTargets, IDirectXVideoProcessorService::GetVideoProcessorRenderTargets, aecbba1e-309c-4668-9e17-d59710d86151, dxva2api/IDirectXVideoProcessorService::GetVideoProcessorRenderTargets, mf.idirectxvideoprocessorservice_getvideoprocessorrendertargets
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
 - IDirectXVideoProcessorService::GetVideoProcessorRenderTargets
 - dxva2api/IDirectXVideoProcessorService::GetVideoProcessorRenderTargets
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
 - IDirectXVideoProcessorService.GetVideoProcessorRenderTargets
---

# IDirectXVideoProcessorService::GetVideoProcessorRenderTargets


## -description

Gets the render target formats that a video processor device supports. The list may include RGB and YUV formats.

## -parameters

### -param VideoProcDeviceGuid [in]

A GUID that identifies the video processor device.
          To get the list of video processor GUIDs, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>.

### -param pVideoDesc [in]

A pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc">DXVA2_VideoDesc</a> structure that describes the video content.

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

<a href="/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice">IDirectXVideoProcessorService</a>