---
UID: NF:dxvahd.IDXVAHD_Device.GetVideoProcessorCaps
title: IDXVAHD_Device::GetVideoProcessorCaps
author: windows-sdk-content
description: Gets the capabilities of one or more Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processors.
old-location: mf\idxvahd_device_getvideoprocessorcaps.htm
old-project: medfound
ms.assetid: d9423b3f-4a4b-49f0-8018-c19a7b663300
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetVideoProcessorCaps, GetVideoProcessorCaps method [Media Foundation], GetVideoProcessorCaps method [Media Foundation],IDXVAHD_Device interface, IDXVAHD_Device interface [Media Foundation],GetVideoProcessorCaps method, IDXVAHD_Device.GetVideoProcessorCaps, IDXVAHD_Device::GetVideoProcessorCaps, dxvahd/IDXVAHD_Device::GetVideoProcessorCaps, mf.idxvahd_device_getvideoprocessorcaps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_SURFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_Device.GetVideoProcessorCaps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXVAHD_Device::GetVideoProcessorCaps


## -description


Gets the capabilities of one or more Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processors.


## -parameters




### -param Count [in]

The number of elements in the <i>pCaps</i> array. This parameter must equal the <b>VideoProcessorCount</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure. Call the <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> method to get this value.


### -param pCaps [out]

A pointer to an array of <a href="https://msdn.microsoft.com/25ec6802-ca6e-42d4-b1d5-de7597e3d042">DXVAHD_VPCAPS</a> structures. The method fills the structures with the capabilities of the video processors supported by the driver.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/3f79ac9c-2aed-4e1c-bf6f-02f9c54d59cd">IDXVAHD_Device</a>
 

 

