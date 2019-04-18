---
UID: NF:dxva2api.IDirectXVideoDecoderService.GetDecoderRenderTargets
title: IDirectXVideoDecoderService::GetDecoderRenderTargets (dxva2api.h)
author: windows-sdk-content
description: Retrieves the supported render targets for a specified decoder device.
old-location: mf\idirectxvideodecoderservice_getdecoderrendertargets.htm
tech.root: medfound
ms.assetid: cde04894-9042-4916-b195-60d84d0f87ec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDecoderRenderTargets, GetDecoderRenderTargets method [Media Foundation], GetDecoderRenderTargets method [Media Foundation],IDirectXVideoDecoderService interface, IDirectXVideoDecoderService interface [Media Foundation],GetDecoderRenderTargets method, IDirectXVideoDecoderService.GetDecoderRenderTargets, IDirectXVideoDecoderService::GetDecoderRenderTargets, cde04894-9042-4916-b195-60d84d0f87ec, dxva2api/IDirectXVideoDecoderService::GetDecoderRenderTargets, mf.idirectxvideodecoderservice_getdecoderrendertargets
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
 - IDirectXVideoDecoderService.GetDecoderRenderTargets
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectXVideoDecoderService::GetDecoderRenderTargets


## -description



Retrieves the supported render targets for a specified decoder device.




## -parameters




### -param Guid [in]

GUID that identifies the decoder device. To get the available device GUIDs, call <a href="https://msdn.microsoft.com/53980b1f-2be1-4267-a581-a4b09255b89f">IDirectXVideoDecoderService::GetDecoderDeviceGuids</a>.


### -param pCount [out]

Receives the number of formats.


### -param pFormats [out]

Receives an array of formats, specified as <b>D3DFORMAT</b> values. The size of the array is retrieved in the <i>pCount</i> parameter. The method allocates the memory for the array. The caller must free the memory by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


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
 

 

