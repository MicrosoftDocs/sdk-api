---
UID: NF:dxva2api.IDirectXVideoProcessor.GetVideoProcessorService
title: IDirectXVideoProcessor::GetVideoProcessorService
author: windows-sdk-content
description: Retrieves the DirectX Video Acceleration (DXVA) video processor service that created this video processor device.
old-location: mf\idirectxvideoprocessor_getvideoprocessorservice.htm
tech.root: medfound
ms.assetid: 920bc584-16ea-4f66-b507-2fe63bfd4fd5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 920bc584-16ea-4f66-b507-2fe63bfd4fd5, GetVideoProcessorService, GetVideoProcessorService method [Media Foundation], GetVideoProcessorService method [Media Foundation],IDirectXVideoProcessor interface, IDirectXVideoProcessor interface [Media Foundation],GetVideoProcessorService method, IDirectXVideoProcessor.GetVideoProcessorService, IDirectXVideoProcessor::GetVideoProcessorService, dxva2api/IDirectXVideoProcessor::GetVideoProcessorService, mf.idirectxvideoprocessor_getvideoprocessorservice
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
 - IDirectXVideoProcessor.GetVideoProcessorService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoProcessor::GetVideoProcessorService


## -description



Retrieves the DirectX Video Acceleration (DXVA) video processor service that created this video processor device.




## -parameters




### -param ppService [out]

Receives a pointer to <a href="https://msdn.microsoft.com/fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688">IDirectXVideoProcessorService</a> interface. The caller must release the interface.


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
 

 

