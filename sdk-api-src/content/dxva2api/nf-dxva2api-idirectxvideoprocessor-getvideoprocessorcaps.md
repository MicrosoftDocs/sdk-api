---
UID: NF:dxva2api.IDirectXVideoProcessor.GetVideoProcessorCaps
title: IDirectXVideoProcessor::GetVideoProcessorCaps (dxva2api.h)
author: windows-sdk-content
description: Retrieves the capabilities of the video processor device.
old-location: mf\idirectxvideoprocessor_getvideoprocessorcaps.htm
tech.root: medfound
ms.assetid: f004d4fb-9fad-44f2-a284-3a612adbaf31
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorCaps, GetVideoProcessorCaps method [Media Foundation], GetVideoProcessorCaps method [Media Foundation],IDirectXVideoProcessor interface, IDirectXVideoProcessor interface [Media Foundation],GetVideoProcessorCaps method, IDirectXVideoProcessor.GetVideoProcessorCaps, IDirectXVideoProcessor::GetVideoProcessorCaps, dxva2api/IDirectXVideoProcessor::GetVideoProcessorCaps, f004d4fb-9fad-44f2-a284-3a612adbaf31, mf.idirectxvideoprocessor_getvideoprocessorcaps
ms.topic: method
f1_keywords:
- dxva2api/IDirectXVideoProcessor.GetVideoProcessorCaps
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
- IDirectXVideoProcessor.GetVideoProcessorCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectXVideoProcessor::GetVideoProcessorCaps


## -description



Retrieves the capabilities of the video processor device.




## -parameters




### -param pCaps [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps">DXVA2_VideoProcessorCaps</a> structure that receives the video processor capabilities.


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




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor">IDirectXVideoProcessor</a>
 

 

