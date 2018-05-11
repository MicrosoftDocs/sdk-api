---
UID: NF:dxva2api.IDirectXVideoProcessorService.GetVideoProcessorRenderTargets
title: IDirectXVideoProcessorService::GetVideoProcessorRenderTargets
author: windows-driver-content
description: Gets the render target formats that a video processor device supports. The list may include RGB and YUV formats.
old-location: mf\idirectxvideoprocessorservice_getvideoprocessorrendertargets.htm
old-project: medfound
ms.assetid: aecbba1e-309c-4668-9e17-d59710d86151
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetVideoProcessorRenderTargets, GetVideoProcessorRenderTargets method [Media Foundation], GetVideoProcessorRenderTargets method [Media Foundation],IDirectXVideoProcessorService interface, IDirectXVideoProcessorService interface [Media Foundation],GetVideoProcessorRenderTargets method, IDirectXVideoProcessorService.GetVideoProcessorRenderTargets, IDirectXVideoProcessorService::GetVideoProcessorRenderTargets, aecbba1e-309c-4668-9e17-d59710d86151, dxva2api/IDirectXVideoProcessorService::GetVideoProcessorRenderTargets, mf.idirectxvideoprocessorservice_getvideoprocessorrendertargets
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
-	IDirectXVideoProcessorService.GetVideoProcessorRenderTargets
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirectXVideoProcessorService::GetVideoProcessorRenderTargets


## -description



          Gets the render target formats that a video processor device supports. The list may include RGB and YUV formats.
        


## -parameters




### -param VideoProcDeviceGuid [in]


            A GUID that identifies the video processor device.
          To get the list of video processor GUIDs, call <a href="https://msdn.microsoft.com/26b52407-7c75-4731-aff3-41376aa9ac3a">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>.


### -param pVideoDesc [in]


            A pointer to a <a href="https://msdn.microsoft.com/0e500a08-a3b5-475c-8bbc-e4b30cce247d">DXVA2_VideoDesc</a> structure that describes the video content.
          


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




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688">IDirectXVideoProcessorService</a>
 

 

