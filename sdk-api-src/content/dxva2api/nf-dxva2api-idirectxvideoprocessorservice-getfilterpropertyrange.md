---
UID: NF:dxva2api.IDirectXVideoProcessorService.GetFilterPropertyRange
title: IDirectXVideoProcessorService::GetFilterPropertyRange (dxva2api.h)
description: Retrieves the range of values for an image filter supported by a video processor device.
helpviewer_keywords: ["0c5f37c6-4220-44ee-9ae3-c31a6454a42a","GetFilterPropertyRange","GetFilterPropertyRange method [Media Foundation]","GetFilterPropertyRange method [Media Foundation]","IDirectXVideoProcessorService interface","IDirectXVideoProcessorService interface [Media Foundation]","GetFilterPropertyRange method","IDirectXVideoProcessorService.GetFilterPropertyRange","IDirectXVideoProcessorService::GetFilterPropertyRange","dxva2api/IDirectXVideoProcessorService::GetFilterPropertyRange","mf.idirectxvideoprocessorservice_getfilterpropertyrange"]
old-location: mf\idirectxvideoprocessorservice_getfilterpropertyrange.htm
tech.root: mf
ms.assetid: 0c5f37c6-4220-44ee-9ae3-c31a6454a42a
ms.date: 12/05/2018
ms.keywords: 0c5f37c6-4220-44ee-9ae3-c31a6454a42a, GetFilterPropertyRange, GetFilterPropertyRange method [Media Foundation], GetFilterPropertyRange method [Media Foundation],IDirectXVideoProcessorService interface, IDirectXVideoProcessorService interface [Media Foundation],GetFilterPropertyRange method, IDirectXVideoProcessorService.GetFilterPropertyRange, IDirectXVideoProcessorService::GetFilterPropertyRange, dxva2api/IDirectXVideoProcessorService::GetFilterPropertyRange, mf.idirectxvideoprocessorservice_getfilterpropertyrange
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
 - IDirectXVideoProcessorService::GetFilterPropertyRange
 - dxva2api/IDirectXVideoProcessorService::GetFilterPropertyRange
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
 - IDirectXVideoProcessorService.GetFilterPropertyRange
---

# IDirectXVideoProcessorService::GetFilterPropertyRange


## -description

Retrieves the range of values for an image filter supported by a video processor device.

## -parameters

### -param VideoProcDeviceGuid [in]

A GUID that identifies the video processor device.
          To get the list of video processor GUIDs, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>.

### -param pVideoDesc [in]

A pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc">DXVA2_VideoDesc</a> structure that describes the video content.

### -param RenderTargetFormat [in]

The format of the render target surface, specified as a <b>D3DFORMAT</b> value. For more information, see the Direct3D documentation. You can also use a FOURCC code to specify a format that is not defined in the <b>D3DFORMAT</b> enumeration. See <a href="/windows/desktop/medfound/video-fourccs">Video FOURCCs</a>.

### -param FilterSetting [in]

The filter setting to query. See <a href="/windows/desktop/medfound/dxva-image-filter-settings">DXVA Image Filter Settings</a>.

### -param pRange [out]

A pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_valuerange">DXVA2_ValueRange</a> structure that receives range of values for the image filter setting specified in <i>FilterSetting</i>.

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