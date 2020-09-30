---
UID: NF:dxva2api.IDirectXVideoProcessorService.RegisterVideoProcessorSoftwareDevice
title: IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice (dxva2api.h)
description: Registers a software video processing device.
helpviewer_keywords: ["3d0bdd60-6cc7-4229-aed9-40b407167456","IDirectXVideoProcessorService interface [Media Foundation]","RegisterVideoProcessorSoftwareDevice method","IDirectXVideoProcessorService.RegisterVideoProcessorSoftwareDevice","IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice","RegisterVideoProcessorSoftwareDevice","RegisterVideoProcessorSoftwareDevice method [Media Foundation]","RegisterVideoProcessorSoftwareDevice method [Media Foundation]","IDirectXVideoProcessorService interface","dxva2api/IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice","mf.idirectxvideoprocessorservice_registervideoprocessorsoftwaredevice"]
old-location: mf\idirectxvideoprocessorservice_registervideoprocessorsoftwaredevice.htm
tech.root: mf
ms.assetid: 3d0bdd60-6cc7-4229-aed9-40b407167456
ms.date: 12/05/2018
ms.keywords: 3d0bdd60-6cc7-4229-aed9-40b407167456, IDirectXVideoProcessorService interface [Media Foundation],RegisterVideoProcessorSoftwareDevice method, IDirectXVideoProcessorService.RegisterVideoProcessorSoftwareDevice, IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice, RegisterVideoProcessorSoftwareDevice, RegisterVideoProcessorSoftwareDevice method [Media Foundation], RegisterVideoProcessorSoftwareDevice method [Media Foundation],IDirectXVideoProcessorService interface, dxva2api/IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice, mf.idirectxvideoprocessorservice_registervideoprocessorsoftwaredevice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice
 - dxva2api/IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoProcessorService.RegisterVideoProcessorSoftwareDevice
---

# IDirectXVideoProcessorService::RegisterVideoProcessorSoftwareDevice


## -description

Registers a software video processing device.

## -parameters

### -param pCallbacks [in]

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

<a href="/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice">IDirectXVideoProcessorService</a>