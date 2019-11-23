---
UID: NF:dxva2api.IDirectXVideoProcessor.GetVideoProcessorService
title: IDirectXVideoProcessor::GetVideoProcessorService (dxva2api.h)

description: Retrieves the DirectX Video Acceleration (DXVA) video processor service that created this video processor device.
old-location: mf\idirectxvideoprocessor_getvideoprocessorservice.htm
tech.root: medfound
ms.assetid: 920bc584-16ea-4f66-b507-2fe63bfd4fd5

ms.date: 12/05/2018
ms.keywords: 920bc584-16ea-4f66-b507-2fe63bfd4fd5, GetVideoProcessorService, GetVideoProcessorService method [Media Foundation], GetVideoProcessorService method [Media Foundation],IDirectXVideoProcessor interface, IDirectXVideoProcessor interface [Media Foundation],GetVideoProcessorService method, IDirectXVideoProcessor.GetVideoProcessorService, IDirectXVideoProcessor::GetVideoProcessorService, dxva2api/IDirectXVideoProcessor::GetVideoProcessorService, mf.idirectxvideoprocessor_getvideoprocessorservice
ms.topic: method
f1_keywords: 
 - "dxva2api/IDirectXVideoProcessor.GetVideoProcessorService"
dev_langs:
 - c++
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
 - IDirectXVideoProcessor.GetVideoProcessorService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectXVideoProcessor::GetVideoProcessorService


## -description



Retrieves the DirectX Video Acceleration (DXVA) video processor service that created this video processor device.




## -parameters




### -param ppService [out]

Receives a pointer to <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice">IDirectXVideoProcessorService</a> interface. The caller must release the interface.


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
 

 

