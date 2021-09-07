---
UID: NF:dxvahd.IDXVAHD_Device.GetVideoProcessorCustomRates
title: IDXVAHD_Device::GetVideoProcessorCustomRates (dxvahd.h)
description: Gets a list of custom rates that a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor supports. Custom rates are used for frame-rate conversion and inverse telecine (IVTC).
helpviewer_keywords: ["GetVideoProcessorCustomRates","GetVideoProcessorCustomRates method [Media Foundation]","GetVideoProcessorCustomRates method [Media Foundation]","IDXVAHD_Device interface","IDXVAHD_Device interface [Media Foundation]","GetVideoProcessorCustomRates method","IDXVAHD_Device.GetVideoProcessorCustomRates","IDXVAHD_Device::GetVideoProcessorCustomRates","dxvahd/IDXVAHD_Device::GetVideoProcessorCustomRates","mf.idxvahd_device_getvideoprocessorcustomrates"]
old-location: mf\idxvahd_device_getvideoprocessorcustomrates.htm
tech.root: mf
ms.assetid: 63e835bb-dda2-4449-8474-219a373da82d
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorCustomRates, GetVideoProcessorCustomRates method [Media Foundation], GetVideoProcessorCustomRates method [Media Foundation],IDXVAHD_Device interface, IDXVAHD_Device interface [Media Foundation],GetVideoProcessorCustomRates method, IDXVAHD_Device.GetVideoProcessorCustomRates, IDXVAHD_Device::GetVideoProcessorCustomRates, dxvahd/IDXVAHD_Device::GetVideoProcessorCustomRates, mf.idxvahd_device_getvideoprocessorcustomrates
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXVAHD_Device::GetVideoProcessorCustomRates
 - dxvahd/IDXVAHD_Device::GetVideoProcessorCustomRates
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_Device.GetVideoProcessorCustomRates
---

# IDXVAHD_Device::GetVideoProcessorCustomRates


## -description

Gets a list of custom rates that a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor supports. Custom rates are used for frame-rate conversion and inverse telecine (IVTC).

## -parameters

### -param pVPGuid [in]

A GUID that identifies the video processor to query. This GUID must equal the value of the <b>VPGuid</b> member from one of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps">DXVAHD_VPCAPS</a> structures retrieved by the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcaps">IDXVAHD_Device::GetVideoProcessorCaps</a> method.

### -param Count [in]

The number of rates to retrieve. This parameter must equal the <b>CustomRateCount</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps">DXVAHD_VPCAPS</a> structure for the video processor.

### -param pRates [out]

A pointer to an array of <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_custom_rate_data">DXVAHD_CUSTOM_RATE_DATA</a> structures. The <i>Count</i> parameter specifies the number of elements in the array. The method fills the array with a list of custom rates.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device">IDXVAHD_Device</a>