---
UID: NF:dxva2api.IDirectXVideoProcessorService.GetFilterPropertyRange
title: IDirectXVideoProcessorService::GetFilterPropertyRange
author: windows-sdk-content
description: Retrieves the range of values for an image filter supported by a video processor device.
old-location: mf\idirectxvideoprocessorservice_getfilterpropertyrange.htm
tech.root: medfound
ms.assetid: 0c5f37c6-4220-44ee-9ae3-c31a6454a42a
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 0c5f37c6-4220-44ee-9ae3-c31a6454a42a, GetFilterPropertyRange, GetFilterPropertyRange method [Media Foundation], GetFilterPropertyRange method [Media Foundation],IDirectXVideoProcessorService interface, IDirectXVideoProcessorService interface [Media Foundation],GetFilterPropertyRange method, IDirectXVideoProcessorService.GetFilterPropertyRange, IDirectXVideoProcessorService::GetFilterPropertyRange, dxva2api/IDirectXVideoProcessorService::GetFilterPropertyRange, mf.idirectxvideoprocessorservice_getfilterpropertyrange
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
 - IDirectXVideoProcessorService.GetFilterPropertyRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoProcessorService::GetFilterPropertyRange


## -description


Retrieves the range of values for an image filter supported by a video processor device.
        


## -parameters




### -param VideoProcDeviceGuid [in]

A GUID that identifies the video processor device.
          To get the list of video processor GUIDs, call <a href="https://msdn.microsoft.com/26b52407-7c75-4731-aff3-41376aa9ac3a">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>.


### -param pVideoDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/0e500a08-a3b5-475c-8bbc-e4b30cce247d">DXVA2_VideoDesc</a> structure that describes the video content.
          


### -param RenderTargetFormat [in]

The format of the render target surface, specified as a <b>D3DFORMAT</b> value. For more information, see the Direct3D documentation. You can also use a FOURCC code to specify a format that is not defined in the <b>D3DFORMAT</b> enumeration. See <a href="https://msdn.microsoft.com/bea4835d-fd7f-4ac3-8466-7f4e0d799a12">Video FOURCCs</a>.
          


### -param FilterSetting [in]

The filter setting to query. See <a href="https://msdn.microsoft.com/6514992e-8188-4d28-879c-547e9b340b28">DXVA Image Filter Settings</a>.
          


### -param pRange [out]

A pointer to a <a href="https://msdn.microsoft.com/e01328bb-9069-4874-aa35-b3c9bc1c6094">DXVA2_ValueRange</a> structure that receives range of values for the image filter setting specified in <i>FilterSetting</i>.
          


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
 

 

