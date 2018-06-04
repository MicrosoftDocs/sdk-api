---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

