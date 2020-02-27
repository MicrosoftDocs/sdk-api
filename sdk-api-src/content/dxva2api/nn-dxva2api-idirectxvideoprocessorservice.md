---
UID: NN:dxva2api.IDirectXVideoProcessorService
title: IDirectXVideoProcessorService (dxva2api.h)
description: Provides access to DirectX Video Acceleration (DXVA) video processing services.
old-location: mf\idirectxvideoprocessorservice.htm
tech.root: medfound
ms.assetid: fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688
ms.date: 12/05/2018
ms.keywords: IDirectXVideoProcessorService, IDirectXVideoProcessorService interface [Media Foundation], IDirectXVideoProcessorService interface [Media Foundation],described, dxva2api/IDirectXVideoProcessorService, fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688, mf.idirectxvideoprocessorservice
f1_keywords:
- dxva2api/IDirectXVideoProcessorService
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dxva2api.h
api_name:
- IDirectXVideoProcessorService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectXVideoProcessorService interface


## -description


Provides access to DirectX Video Acceleration (DXVA) video processing services.

Use this interface to query which hardware-accelerated video processing operations are available and to create DXVA video processor devices. To obtain a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice">IDirect3DDeviceManager9::GetVideoService</a> or <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice">DXVA2CreateVideoService</a> with the interface identifier <b>IID_IDirectXVideoProcessorService</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectXVideoProcessorService</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice">IDirectXVideoAccelerationService</a>. <b>IDirectXVideoProcessorService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectXVideoProcessorService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor">CreateVideoProcessor</a>
</td>
<td align="left" width="63%">
Creates a video processor device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getfilterpropertyrange">GetFilterPropertyRange</a>
</td>
<td align="left" width="63%">
Gets the range of values for an image filter supported by a video processor device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getprocamprange">GetProcAmpRange</a>
</td>
<td align="left" width="63%">
Gets the range of values for a video processor (ProcAmp) setting.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps">GetVideoProcessorCaps</a>
</td>
<td align="left" width="63%">
Gets the capabilities of a specified video processor device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids">GetVideoProcessorDeviceGuids</a>
</td>
<td align="left" width="63%">
Gets an array of GUIDs that identifies the video processors supported by the graphics hardware.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets">GetVideoProcessorRenderTargets</a>
</td>
<td align="left" width="63%">
Gets the supported render targets for a specified video processor device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats">GetVideoProcessorSubStreamFormats</a>
</td>
<td align="left" width="63%">
Gets a list of substream formats supported by a specified video processor device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-registervideoprocessorsoftwaredevice">RegisterVideoProcessorSoftwareDevice</a>
</td>
<td align="left" width="63%">
Gets a software video processing device.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice">IDirectXVideoAccelerationService</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

