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

# IDirectXVideoDecoder::GetCreationParameters


## -description



          Retrieves the parameters that were used to create this device.
        


## -parameters




### -param pDeviceGuid [out]

Receives the device GUID. This parameter can be <b>NULL</b>.


### -param pVideoDesc [out]

Pointer to a <a href="https://msdn.microsoft.com/0e500a08-a3b5-475c-8bbc-e4b30cce247d">DXVA2_VideoDesc</a> structure that receives a description of the video format. This parameter can be <b>NULL</b>.


### -param pConfig [out]

Pointer to a <a href="https://msdn.microsoft.com/1515cfa9-24ff-4c65-adca-f4143d36685c">DXVA2_ConfigPictureDecode</a> structure structure that receives the decoder configuration. This parameter can be <b>NULL</b>.


### -param pDecoderRenderTargets




### -param pNumSurfaces [out]

Receives the number of elements in the <i>pppDecoderRenderTargets</i> array. This parameter can be <b>NULL</b>.


#### - pppDecoderRenderTargets [out]

Receives an array of <b>IDirect3DSurface9</b> interface pointers. These pointers represent the decoder render targets. The method allocates the memory for the array and calls <b>AddRef</b> on each of the pointers. The caller must release the pointers and call <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to free the memory for the array. This parameter can be <b>NULL</b>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. At least one parameter must be non-<b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



You can set any parameter to <b>NULL</b> if you are not interested in the result. At least one parameter must be non-<b>NULL</b>.

If you specify a non-<b>NULL</b> value for <i>pppDecoderRenderTargets</i> (to receive the render target surfaces), then <i>pNumSurfaces</i> cannot be <b>NULL</b>, because it receives the size of the array returned in <i>pppDecoderRenderTargets</i>.




## -see-also




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/116c19a3-39be-4f96-969f-f3d62ed33a70">IDirectXVideoDecoder</a>
 

 

