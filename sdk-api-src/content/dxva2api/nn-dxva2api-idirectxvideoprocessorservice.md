---
UID: NN:dxva2api.IDirectXVideoProcessorService
title: IDirectXVideoProcessorService
author: windows-sdk-content
description: Provides access to DirectX Video Acceleration (DXVA) video processing services.
old-location: mf\idirectxvideoprocessorservice.htm
tech.root: medfound
ms.assetid: fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectXVideoProcessorService, IDirectXVideoProcessorService interface [Media Foundation], IDirectXVideoProcessorService interface [Media Foundation],described, dxva2api/IDirectXVideoProcessorService, fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688, mf.idirectxvideoprocessorservice
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoProcessorService interface


## -description


Provides access to DirectX Video Acceleration (DXVA) video processing services.

Use this interface to query which hardware-accelerated video processing operations are available and to create DXVA video processor devices. To obtain a pointer to this interface, call <a href="https://msdn.microsoft.com/2e62a750-3017-4dd7-9fbc-e2c641f6cf10">IDirect3DDeviceManager9::GetVideoService</a> or <a href="https://msdn.microsoft.com/e62dbacb-f638-4307-ba56-88415d881fc9">DXVA2CreateVideoService</a> with the interface identifier <b>IID_IDirectXVideoProcessorService</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectXVideoProcessorService</b> interface inherits from <a href="https://msdn.microsoft.com/50a2d8f7-d7c9-4d50-88cc-f6c8562fbb17">IDirectXVideoAccelerationService</a>. <b>IDirectXVideoProcessorService</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/18178a10-f902-4d25-992e-a27145204321">CreateVideoProcessor</a>
</td>
<td align="left" width="63%">
Creates a video processor device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c5f37c6-4220-44ee-9ae3-c31a6454a42a">GetFilterPropertyRange</a>
</td>
<td align="left" width="63%">
Gets the range of values for an image filter supported by a video processor device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4945e2f-6907-4e02-9719-89c8e0bf1404">GetProcAmpRange</a>
</td>
<td align="left" width="63%">
Gets the range of values for a video processor (ProcAmp) setting.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb94f221-cca7-48e1-96ef-b5a6f7c24a47">GetVideoProcessorCaps</a>
</td>
<td align="left" width="63%">
Gets the capabilities of a specified video processor device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26b52407-7c75-4731-aff3-41376aa9ac3a">GetVideoProcessorDeviceGuids</a>
</td>
<td align="left" width="63%">
Gets an array of GUIDs that identifies the video processors supported by the graphics hardware.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aecbba1e-309c-4668-9e17-d59710d86151">GetVideoProcessorRenderTargets</a>
</td>
<td align="left" width="63%">
Gets the supported render targets for a specified video processor device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10ad4d8d-9b5e-4f77-8244-c29a0e14a5b1">GetVideoProcessorSubStreamFormats</a>
</td>
<td align="left" width="63%">
Gets a list of substream formats supported by a specified video processor device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d0bdd60-6cc7-4229-aed9-40b407167456">RegisterVideoProcessorSoftwareDevice</a>
</td>
<td align="left" width="63%">
Gets a software video processing device.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/50a2d8f7-d7c9-4d50-88cc-f6c8562fbb17">IDirectXVideoAccelerationService</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

