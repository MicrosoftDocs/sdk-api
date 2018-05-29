---
UID: NF:dxva2api.IDirectXVideoProcessor.GetCreationParameters
title: IDirectXVideoProcessor::GetCreationParameters
author: windows-sdk-content
description: Retrieves the parameters that were used to create this device.
old-location: mf\idirectxvideoprocessor_getcreationparameters.htm
old-project: medfound
ms.assetid: e9ea3311-8642-4651-b9da-fbba08ec92fb
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetCreationParameters, GetCreationParameters method [Media Foundation], GetCreationParameters method [Media Foundation],IDirectXVideoProcessor interface, IDirectXVideoProcessor interface [Media Foundation],GetCreationParameters method, IDirectXVideoProcessor.GetCreationParameters, IDirectXVideoProcessor::GetCreationParameters, dxva2api/IDirectXVideoProcessor::GetCreationParameters, e9ea3311-8642-4651-b9da-fbba08ec92fb, mf.idirectxvideoprocessor_getcreationparameters
ms.prod: windows
ms.technology: windows-sdk
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
-	IDirectXVideoProcessor.GetCreationParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirectXVideoProcessor::GetCreationParameters


## -description



Retrieves the parameters that were used to create this device.




## -parameters




### -param pDeviceGuid [out]

Receives the device GUID. This parameter can be <b>NULL</b>.


### -param pVideoDesc [out]

Pointer to a <a href="https://msdn.microsoft.com/0e500a08-a3b5-475c-8bbc-e4b30cce247d">DXVA2_VideoDesc</a> structure allocated by the caller. The method fills the structure with a description of the video format. This parameter can be <b>NULL</b>.


### -param pRenderTargetFormat [out]

Receives the render target format, specified as a <b>D3DFORMAT</b> value. For more information, see the Direct3D documentation. This parameter can be <b>NULL</b>.


### -param pMaxNumSubStreams [out]

Receives the maximum number of streams supported by the device. This parameter can be <b>NULL</b>.


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




## -see-also




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/a9bc3162-4f37-4f0b-8a8e-8ebeb8f0d8d5">IDirectXVideoProcessor</a>
 

 

