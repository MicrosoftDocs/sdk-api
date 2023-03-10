---
UID: NF:dxvahd.IDXVAHD_Device.GetVideoProcessorCaps
title: IDXVAHD_Device::GetVideoProcessorCaps (dxvahd.h)
description: Gets the capabilities of one or more Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processors.
helpviewer_keywords: ["GetVideoProcessorCaps","GetVideoProcessorCaps method [Media Foundation]","GetVideoProcessorCaps method [Media Foundation]","IDXVAHD_Device interface","IDXVAHD_Device interface [Media Foundation]","GetVideoProcessorCaps method","IDXVAHD_Device.GetVideoProcessorCaps","IDXVAHD_Device::GetVideoProcessorCaps","dxvahd/IDXVAHD_Device::GetVideoProcessorCaps","mf.idxvahd_device_getvideoprocessorcaps"]
old-location: mf\idxvahd_device_getvideoprocessorcaps.htm
tech.root: mf
ms.assetid: d9423b3f-4a4b-49f0-8018-c19a7b663300
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorCaps, GetVideoProcessorCaps method [Media Foundation], GetVideoProcessorCaps method [Media Foundation],IDXVAHD_Device interface, IDXVAHD_Device interface [Media Foundation],GetVideoProcessorCaps method, IDXVAHD_Device.GetVideoProcessorCaps, IDXVAHD_Device::GetVideoProcessorCaps, dxvahd/IDXVAHD_Device::GetVideoProcessorCaps, mf.idxvahd_device_getvideoprocessorcaps
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
 - IDXVAHD_Device::GetVideoProcessorCaps
 - dxvahd/IDXVAHD_Device::GetVideoProcessorCaps
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
 - IDXVAHD_Device.GetVideoProcessorCaps
---

# IDXVAHD_Device::GetVideoProcessorCaps


## -description

Gets the capabilities of one or more Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processors.

## -parameters

### -param Count [in]

The number of elements in the <i>pCaps</i> array. This parameter must equal the <b>VideoProcessorCount</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure. Call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> method to get this value.

### -param pCaps [out]

A pointer to an array of <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps">DXVAHD_VPCAPS</a> structures. The method fills the structures with the capabilities of the video processors supported by the driver.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device">IDXVAHD_Device</a>