---
UID: NN:dxva2api.IDirectXVideoDecoderService
title: IDirectXVideoDecoderService
author: windows-driver-content
description: Provides access to DirectX Video Acceleration (DXVA) decoder services.
old-location: mf\idirectxvideodecoderservice.htm
old-project: medfound
ms.assetid: eeb62178-b54d-45d3-a584-75865f0662fa
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IDirectXVideoDecoderService, IDirectXVideoDecoderService interface [Media Foundation], IDirectXVideoDecoderService interface [Media Foundation], described, dxva2api/IDirectXVideoDecoderService, eeb62178-b54d-45d3-a584-75865f0662fa, mf.idirectxvideodecoderservice
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DXVA2_SurfaceType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva2api.h
api_name:
-	IDirectXVideoDecoderService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirectXVideoDecoderService interface


## -description


Provides access to DirectX Video Acceleration (DXVA) decoder services. Use this interface to query which hardware-accelerated decoding operations are available and to create DXVA video decoder devices. 

To get a pointer to this interface, call <a href="https://msdn.microsoft.com/2e62a750-3017-4dd7-9fbc-e2c641f6cf10">IDirect3DDeviceManager9::GetVideoService</a> or <a href="https://msdn.microsoft.com/e62dbacb-f638-4307-ba56-88415d881fc9">DXVA2CreateVideoService</a> with the interface identifier IID_IDirectXVideoDecoderService.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectXVideoDecoderService</b> interface inherits from <a href="https://msdn.microsoft.com/50a2d8f7-d7c9-4d50-88cc-f6c8562fbb17">IDirectXVideoAccelerationService</a>. <b>IDirectXVideoDecoderService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectXVideoDecoderService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a799411-e8d5-4ab8-b52f-7198af9a4f2b">CreateVideoDecoder</a>
</td>
<td align="left" width="63%">
Creates a video decoder device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d2c24f3-9066-4e8b-aad6-98b7245088a5">GetDecoderConfigurations</a>
</td>
<td align="left" width="63%">
Retrieves the configurations that are available for a decoder device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53980b1f-2be1-4267-a581-a4b09255b89f">GetDecoderDeviceGuids</a>
</td>
<td align="left" width="63%">
Retrieves an array of GUIDs that identifies the decoder devices supported by the graphics hardware.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cde04894-9042-4916-b195-60d84d0f87ec">GetDecoderRenderTargets</a>
</td>
<td align="left" width="63%">
Retrieves the supported render targets for a specified decoder device.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/50a2d8f7-d7c9-4d50-88cc-f6c8562fbb17">IDirectXVideoAccelerationService</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

