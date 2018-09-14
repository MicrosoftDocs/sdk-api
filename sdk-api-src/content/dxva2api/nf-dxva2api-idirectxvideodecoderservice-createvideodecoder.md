---
UID: NF:dxva2api.IDirectXVideoDecoderService.CreateVideoDecoder
title: IDirectXVideoDecoderService::CreateVideoDecoder
author: windows-sdk-content
description: Creates a video decoder device.
old-location: mf\idirectxvideodecoderservice_createvideodecoder.htm
tech.root: medfound
ms.assetid: 2a799411-e8d5-4ab8-b52f-7198af9a4f2b
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 2a799411-e8d5-4ab8-b52f-7198af9a4f2b, CreateVideoDecoder, CreateVideoDecoder method [Media Foundation], CreateVideoDecoder method [Media Foundation],IDirectXVideoDecoderService interface, IDirectXVideoDecoderService interface [Media Foundation],CreateVideoDecoder method, IDirectXVideoDecoderService.CreateVideoDecoder, IDirectXVideoDecoderService::CreateVideoDecoder, dxva2api/IDirectXVideoDecoderService::CreateVideoDecoder, mf.idirectxvideodecoderservice_createvideodecoder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDirectXVideoDecoderService.CreateVideoDecoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoDecoderService::CreateVideoDecoder


## -description



Creates a video decoder device.




## -parameters




### -param Guid [in]

GUID that specifies the decoder device to create. To get the available device GUIDs, call <a href="https://msdn.microsoft.com/53980b1f-2be1-4267-a581-a4b09255b89f">IDirectXVideoDecoderService::GetDecoderDeviceGuids</a>.


### -param pVideoDesc [in]

Pointer to a <a href="https://msdn.microsoft.com/0e500a08-a3b5-475c-8bbc-e4b30cce247d">DXVA2_VideoDesc</a> structure that describes the video content.


### -param pConfig [in]

Pointer to a <a href="https://msdn.microsoft.com/1515cfa9-24ff-4c65-adca-f4143d36685c">DXVA2_ConfigPictureDecode</a> structure that specifies the decoder configuration.


### -param ppDecoderRenderTargets [in]

Pointer to an array of <b>IDirect3DSurface9</b> pointers containing pointers to the decoder render targets. To create these surfaces, call <a href="https://msdn.microsoft.com/34ed2029-7c79-45ce-962d-df4970babb23">IDirectXVideoAccelerationService::CreateSurface</a>. Specify DXVA2_VideoDecoderRenderTarget for the <i>DxvaType</i> parameter.


### -param NumRenderTargets

TBD


### -param ppDecode [out]

Receives a pointer to the decoder's <a href="https://msdn.microsoft.com/116c19a3-39be-4f96-969f-f3d62ed33a70">IDirectXVideoDecoder</a> interface. The caller must release the interface.


#### - NumSurfaces [in]

Size of the <i>ppDecoderRenderTargets</i> array. This value cannot be zero.


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




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/eeb62178-b54d-45d3-a584-75865f0662fa">IDirectXVideoDecoderService</a>
 

 

