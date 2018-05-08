---
UID: NF:dxva2api.IDirectXVideoDecoder.GetCreationParameters
title: IDirectXVideoDecoder::GetCreationParameters
author: windows-driver-content
description: Retrieves the parameters that were used to create this device.
old-location: mf\idirectxvideodecoder_getcreationparameters.htm
old-project: medfound
ms.assetid: 5e1a4f6b-22f3-40ae-8990-88ecb5b16d44
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 5e1a4f6b-22f3-40ae-8990-88ecb5b16d44, GetCreationParameters, GetCreationParameters method [Media Foundation], GetCreationParameters method [Media Foundation],IDirectXVideoDecoder interface, IDirectXVideoDecoder interface [Media Foundation],GetCreationParameters method, IDirectXVideoDecoder.GetCreationParameters, IDirectXVideoDecoder::GetCreationParameters, dxva2api/IDirectXVideoDecoder::GetCreationParameters, mf.idirectxvideodecoder_getcreationparameters
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
req.typenames: DXVA2_SurfaceType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva2api.h
api_name:
-	IDirectXVideoDecoder.GetCreationParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

