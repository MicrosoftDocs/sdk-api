---
UID: NF:dxva2api.IDirectXVideoProcessorService.RegisterVideoProcessorSoftwareDevice
title: IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice
author: windows-sdk-content
description: Registers a software video processing device.
old-location: mf\idirectxvideoprocessorservice_registervideoprocessorsoftwaredevice.htm
tech.root: MedFound
ms.assetid: 3d0bdd60-6cc7-4229-aed9-40b407167456
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 3d0bdd60-6cc7-4229-aed9-40b407167456, IDirectXVideoProcessorService interface [Media Foundation],RegisterVideoProcessorSoftwareDevice method, IDirectXVideoProcessorService.RegisterVideoProcessorSoftwareDevice, IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice, RegisterVideoProcessorSoftwareDevice, RegisterVideoProcessorSoftwareDevice method [Media Foundation], RegisterVideoProcessorSoftwareDevice method [Media Foundation],IDirectXVideoProcessorService interface, dxva2api/IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice, mf.idirectxvideoprocessorservice_registervideoprocessorsoftwaredevice
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
 - IDirectXVideoProcessorService.RegisterVideoProcessorSoftwareDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice


## -description



Registers a software video processing device.




## -parameters




### -param pCallbacks

TBD




#### - pVideoProcessorInitFunction [in]

Pointer to an initialization function.


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
 

 

