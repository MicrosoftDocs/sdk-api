---
UID: NF:dxva2api.IDirectXVideoProcessorService.GetVideoProcessorCaps
title: IDirectXVideoProcessorService::GetVideoProcessorCaps
author: windows-sdk-content
description: Gets the capabilities of a specified video processor device.
old-location: mf\idirectxvideoprocessorservice_getvideoprocessorcaps.htm
old-project: medfound
ms.assetid: bb94f221-cca7-48e1-96ef-b5a6f7c24a47
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetVideoProcessorCaps, GetVideoProcessorCaps method [Media Foundation], GetVideoProcessorCaps method [Media Foundation],IDirectXVideoProcessorService interface, IDirectXVideoProcessorService interface [Media Foundation],GetVideoProcessorCaps method, IDirectXVideoProcessorService.GetVideoProcessorCaps, IDirectXVideoProcessorService::GetVideoProcessorCaps, bb94f221-cca7-48e1-96ef-b5a6f7c24a47, dxva2api/IDirectXVideoProcessorService::GetVideoProcessorCaps, mf.idirectxvideoprocessorservice_getvideoprocessorcaps
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
-	IDirectXVideoProcessorService.GetVideoProcessorCaps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirectXVideoProcessorService::GetVideoProcessorCaps


## -description



          Gets the capabilities of a specified video processor device.
        


## -parameters




### -param VideoProcDeviceGuid [in]


            A GUID that identifies the video processor device. To get the list of video processor GUIDs, call <a href="https://msdn.microsoft.com/26b52407-7c75-4731-aff3-41376aa9ac3a">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>.


### -param pVideoDesc [in]


            A pointer to a <a href="https://msdn.microsoft.com/0e500a08-a3b5-475c-8bbc-e4b30cce247d">DXVA2_VideoDesc</a> structure that describes the video content.
          


### -param RenderTargetFormat [in]


            The format of the render target surface, specified as a <b>D3DFORMAT</b> value. For more information, see the Direct3D documentation. You can also use a FOURCC code to specify a format that is not defined in the <b>D3DFORMAT</b> enumeration. See <a href="https://msdn.microsoft.com/bea4835d-fd7f-4ac3-8466-7f4e0d799a12">Video FOURCCs</a>.
          


### -param pCaps [out]


            A pointer to a <a href="https://msdn.microsoft.com/cff01719-e653-4ea1-a177-9a6948b0da56">DXVA2_VideoProcessorCaps</a> structure that receives the video processor capabilities.
          


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
 

 

