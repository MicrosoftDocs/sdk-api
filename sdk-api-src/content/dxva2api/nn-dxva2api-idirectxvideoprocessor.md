---
UID: NN:dxva2api.IDirectXVideoProcessor
title: IDirectXVideoProcessor (dxva2api.h)

description: Represents a DirectX Video Acceleration (DXVA) video processor device.
old-location: mf\idirectxvideoprocessor.htm
tech.root: medfound
ms.assetid: a9bc3162-4f37-4f0b-8a8e-8ebeb8f0d8d5

ms.date: 12/05/2018
ms.keywords: IDirectXVideoProcessor, IDirectXVideoProcessor interface [Media Foundation], IDirectXVideoProcessor interface [Media Foundation],described, a9bc3162-4f37-4f0b-8a8e-8ebeb8f0d8d5, dxva2api/IDirectXVideoProcessor, mf.idirectxvideoprocessor
ms.topic: interface
f1_keywords: 
 - "dxva2api/IDirectXVideoProcessor"
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
 - IDirectXVideoProcessor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectXVideoProcessor interface


## -description


Represents a DirectX Video Acceleration (DXVA) video processor device. To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor">IDirectXVideoProcessorService::CreateVideoProcessor</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectXVideoProcessor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectXVideoProcessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectXVideoProcessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-getcreationparameters">GetCreationParameters</a>
</td>
<td align="left" width="63%">
Retrieves the parameters that were used to create this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-getfilterpropertyrange">GetFilterPropertyRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for an image filter supported by this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-getprocamprange">GetProcAmpRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for a video processor (ProcAmp) setting on this video processor device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-getvideoprocessorcaps">GetVideoProcessorCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the video processor device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-getvideoprocessorservice">GetVideoProcessorService</a>
</td>
<td align="left" width="63%">
Retrieves the DXVA video processor service that created this video processor device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt">VideoProcessBlt</a>
</td>
<td align="left" width="63%">
Performs a video process operation on one or more input samples and writes the result to a Direct3D9 surface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

