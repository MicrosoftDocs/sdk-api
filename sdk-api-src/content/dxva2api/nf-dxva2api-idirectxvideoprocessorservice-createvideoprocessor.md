---
UID: NF:dxva2api.IDirectXVideoProcessorService.CreateVideoProcessor
title: IDirectXVideoProcessorService::CreateVideoProcessor (dxva2api.h)
description: Creates a video processor device.
helpviewer_keywords: ["18178a10-f902-4d25-992e-a27145204321","CreateVideoProcessor","CreateVideoProcessor method [Media Foundation]","CreateVideoProcessor method [Media Foundation]","IDirectXVideoProcessorService interface","IDirectXVideoProcessorService interface [Media Foundation]","CreateVideoProcessor method","IDirectXVideoProcessorService.CreateVideoProcessor","IDirectXVideoProcessorService::CreateVideoProcessor","dxva2api/IDirectXVideoProcessorService::CreateVideoProcessor","mf.idirectxvideoprocessorservice_createvideoprocessor"]
old-location: mf\idirectxvideoprocessorservice_createvideoprocessor.htm
tech.root: mf
ms.assetid: 18178a10-f902-4d25-992e-a27145204321
ms.date: 12/05/2018
ms.keywords: 18178a10-f902-4d25-992e-a27145204321, CreateVideoProcessor, CreateVideoProcessor method [Media Foundation], CreateVideoProcessor method [Media Foundation],IDirectXVideoProcessorService interface, IDirectXVideoProcessorService interface [Media Foundation],CreateVideoProcessor method, IDirectXVideoProcessorService.CreateVideoProcessor, IDirectXVideoProcessorService::CreateVideoProcessor, dxva2api/IDirectXVideoProcessorService::CreateVideoProcessor, mf.idirectxvideoprocessorservice_createvideoprocessor
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
 - IDirectXVideoProcessorService::CreateVideoProcessor
 - dxva2api/IDirectXVideoProcessorService::CreateVideoProcessor
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
 - IDirectXVideoProcessorService.CreateVideoProcessor
---

# IDirectXVideoProcessorService::CreateVideoProcessor


## -description

Creates a video processor device.

## -parameters

### -param VideoProcDeviceGuid [in]

A GUID that specifies the video processor to create.
          To get the list of video processor GUIDs, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>.

### -param pVideoDesc [in]

A pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc">DXVA2_VideoDesc</a> structure that describes the video content.

### -param RenderTargetFormat [in]

The format of the render target surface, specified as a <b>D3DFORMAT</b> value. For more information, see the Direct3D documentation. You can also use a FOURCC code to specify a format that is not defined in the <b>D3DFORMAT</b> enumeration. See <a href="/windows/desktop/medfound/video-fourccs">Video FOURCCs</a>.

### -param MaxNumSubStreams [in]

The maximum number of substreams that will be used with this device.

### -param ppVidProcess [out]

Receives a pointer to the video processor's <a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor">IDirectXVideoProcessor</a> interface. The caller must release the interface.

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