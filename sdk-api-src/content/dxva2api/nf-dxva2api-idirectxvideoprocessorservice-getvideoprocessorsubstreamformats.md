---
UID: NF:dxva2api.IDirectXVideoProcessorService.GetVideoProcessorSubStreamFormats
title: IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats (dxva2api.h)
description: Gets a list of substream formats supported by a specified video processor device.
helpviewer_keywords: ["10ad4d8d-9b5e-4f77-8244-c29a0e14a5b1","GetVideoProcessorSubStreamFormats","GetVideoProcessorSubStreamFormats method [Media Foundation]","GetVideoProcessorSubStreamFormats method [Media Foundation]","IDirectXVideoProcessorService interface","IDirectXVideoProcessorService interface [Media Foundation]","GetVideoProcessorSubStreamFormats method","IDirectXVideoProcessorService.GetVideoProcessorSubStreamFormats","IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats","dxva2api/IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats","mf.idirectxvideoprocessorservice_getvideoprocessorsubstreamformats"]
old-location: mf\idirectxvideoprocessorservice_getvideoprocessorsubstreamformats.htm
tech.root: mf
ms.assetid: 10ad4d8d-9b5e-4f77-8244-c29a0e14a5b1
ms.date: 12/05/2018
ms.keywords: 10ad4d8d-9b5e-4f77-8244-c29a0e14a5b1, GetVideoProcessorSubStreamFormats, GetVideoProcessorSubStreamFormats method [Media Foundation], GetVideoProcessorSubStreamFormats method [Media Foundation],IDirectXVideoProcessorService interface, IDirectXVideoProcessorService interface [Media Foundation],GetVideoProcessorSubStreamFormats method, IDirectXVideoProcessorService.GetVideoProcessorSubStreamFormats, IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats, dxva2api/IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats, mf.idirectxvideoprocessorservice_getvideoprocessorsubstreamformats
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
 - IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats
 - dxva2api/IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats
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
 - IDirectXVideoProcessorService.GetVideoProcessorSubStreamFormats
---

# IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats


## -description

Gets a list of substream formats supported by a specified video processor device.

## -parameters

### -param VideoProcDeviceGuid [in]

A GUID that identifies the video processor device. 
          To get the list of video processor GUIDs, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>.

### -param pVideoDesc [in]

A pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc">DXVA2_VideoDesc</a> structure that describes the video content.

### -param RenderTargetFormat [in]

The format of the render target surface, specified as a <b>D3DFORMAT</b> value. For more information, see the Direct3D documentation. You can also use a FOURCC code to specify a format that is not defined in the <b>D3DFORMAT</b> enumeration. See <a href="/windows/desktop/medfound/video-fourccs">Video FOURCCs</a>.

### -param pCount [out]

Receives the number of elements returned in the <i>ppFormats</i> array.

### -param pFormats [out]

Receives an array of <b>D3DFORMAT</b> values. The caller must free the array by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. The array can contain both RGB and YUB pixel formats.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice">IDirectXVideoProcessorService</a>