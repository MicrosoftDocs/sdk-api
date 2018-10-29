---
UID: NF:dxvahd.IDXVAHD_Device.GetVideoProcessorCustomRates
title: IDXVAHD_Device::GetVideoProcessorCustomRates
author: windows-sdk-content
description: Gets a list of custom rates that a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor supports. Custom rates are used for frame-rate conversion and inverse telecine (IVTC).
old-location: mf\idxvahd_device_getvideoprocessorcustomrates.htm
tech.root: medfound
ms.assetid: 63e835bb-dda2-4449-8474-219a373da82d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetVideoProcessorCustomRates, GetVideoProcessorCustomRates method [Media Foundation], GetVideoProcessorCustomRates method [Media Foundation],IDXVAHD_Device interface, IDXVAHD_Device interface [Media Foundation],GetVideoProcessorCustomRates method, IDXVAHD_Device.GetVideoProcessorCustomRates, IDXVAHD_Device::GetVideoProcessorCustomRates, dxvahd/IDXVAHD_Device::GetVideoProcessorCustomRates, mf.idxvahd_device_getvideoprocessorcustomrates
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_Device.GetVideoProcessorCustomRates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXVAHD_Device::GetVideoProcessorCustomRates


## -description


Gets a list of custom rates that a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor supports. Custom rates are used for frame-rate conversion and inverse telecine (IVTC).


## -parameters




### -param pVPGuid [in]

A GUID that identifies the video processor to query. This GUID must equal the valud of the <b>VPGuid</b> member from one of the <a href="https://msdn.microsoft.com/25ec6802-ca6e-42d4-b1d5-de7597e3d042">DXVAHD_VPCAPS</a> structures retrieved by the <a href="https://msdn.microsoft.com/d9423b3f-4a4b-49f0-8018-c19a7b663300">IDXVAHD_Device::GetVideoProcessorCaps</a> method.


### -param Count [in]

The number of rates to retrieve. This parameter must equal the <b>CustomRateCount</b> member of the <a href="https://msdn.microsoft.com/25ec6802-ca6e-42d4-b1d5-de7597e3d042">DXVAHD_VPCAPS</a> structure for the video processor. 


### -param pRates [out]

A pointer to an array of <a href="https://msdn.microsoft.com/12cac4a8-cfdf-484c-8443-ef47dd3a152b">DXVAHD_CUSTOM_RATE_DATA</a> structures. The <i>Count</i> parameter specifies the number of elements in the array. The method fills the array with a list of custom rates.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/3f79ac9c-2aed-4e1c-bf6f-02f9c54d59cd">IDXVAHD_Device</a>
 

 

