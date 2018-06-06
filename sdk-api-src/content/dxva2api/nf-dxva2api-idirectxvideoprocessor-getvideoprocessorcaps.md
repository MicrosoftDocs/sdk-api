---
UID: NF:dxva2api.IDirectXVideoProcessor.GetVideoProcessorCaps
title: IDirectXVideoProcessor::GetVideoProcessorCaps
author: windows-sdk-content
description: Retrieves the capabilities of the video processor device.
old-location: mf\idirectxvideoprocessor_getvideoprocessorcaps.htm
old-project: medfound
ms.assetid: f004d4fb-9fad-44f2-a284-3a612adbaf31
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetVideoProcessorCaps, GetVideoProcessorCaps method [Media Foundation], GetVideoProcessorCaps method [Media Foundation],IDirectXVideoProcessor interface, IDirectXVideoProcessor interface [Media Foundation],GetVideoProcessorCaps method, IDirectXVideoProcessor.GetVideoProcessorCaps, IDirectXVideoProcessor::GetVideoProcessorCaps, dxva2api/IDirectXVideoProcessor::GetVideoProcessorCaps, f004d4fb-9fad-44f2-a284-3a612adbaf31, mf.idirectxvideoprocessor_getvideoprocessorcaps
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
tech.root: 
req.typenames: DXVA2_SurfaceType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoProcessor.GetVideoProcessorCaps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirectXVideoProcessor::GetVideoProcessorCaps


## -description



Retrieves the capabilities of the video processor device.




## -parameters




### -param pCaps [out]

Pointer to a <a href="https://msdn.microsoft.com/cff01719-e653-4ea1-a177-9a6948b0da56">DXVA2_VideoProcessorCaps</a> structure that receives the video processor capabilities.


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



<a href="https://msdn.microsoft.com/a9bc3162-4f37-4f0b-8a8e-8ebeb8f0d8d5">IDirectXVideoProcessor</a>
 

 

