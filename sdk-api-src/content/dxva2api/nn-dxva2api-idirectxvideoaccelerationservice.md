---
UID: NN:dxva2api.IDirectXVideoAccelerationService
title: IDirectXVideoAccelerationService
author: windows-sdk-content
description: Provides DirectX Video Acceleration (DXVA) services from a Direct3D device.
old-location: mf\idirectxvideoaccelerationservice.htm
tech.root: medfound
ms.assetid: 50a2d8f7-d7c9-4d50-88cc-f6c8562fbb17
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 50a2d8f7-d7c9-4d50-88cc-f6c8562fbb17, IDirectXVideoAccelerationService, IDirectXVideoAccelerationService interface [Media Foundation], IDirectXVideoAccelerationService interface [Media Foundation],described, dxva2api/IDirectXVideoAccelerationService, mf.idirectxvideoaccelerationservice
ms.prod: windows
ms.technology: windows-sdk
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
 - IDirectXVideoAccelerationService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoAccelerationService interface


## -description


Provides DirectX Video Acceleration (DXVA) services from a Direct3D device. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/2e62a750-3017-4dd7-9fbc-e2c641f6cf10">IDirect3DDeviceManager9::GetVideoService</a> or <a href="https://msdn.microsoft.com/e62dbacb-f638-4307-ba56-88415d881fc9">DXVA2CreateVideoService</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectXVideoAccelerationService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectXVideoAccelerationService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectXVideoAccelerationService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34ed2029-7c79-45ce-962d-df4970babb23">CreateSurface</a>
</td>
<td align="left" width="63%">
Creates a DirectX Video Acceleration (DXVA) video processor or DXVA decoder render target.
        

</td>
</tr>
</table> 


## -remarks



This is the base interface for DXVA services. The Direct3D device can support any of the following DXVA services, which derive from <b>IDirectXVideoAccelerationService</b>:

<ul>
<li>Video decoding: <a href="https://msdn.microsoft.com/eeb62178-b54d-45d3-a584-75865f0662fa">IDirectXVideoDecoderService</a>
</li>
<li>Video processing: <a href="https://msdn.microsoft.com/fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688">IDirectXVideoProcessorService</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

