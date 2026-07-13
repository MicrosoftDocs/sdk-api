---
UID: NF:dxvahd.IDXVAHD_Device.GetVideoProcessorDeviceCaps
title: IDXVAHD_Device::GetVideoProcessorDeviceCaps (dxvahd.h)
description: Gets the capabilities of the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["GetVideoProcessorDeviceCaps","GetVideoProcessorDeviceCaps method [Media Foundation]","GetVideoProcessorDeviceCaps method [Media Foundation]","IDXVAHD_Device interface","IDXVAHD_Device interface [Media Foundation]","GetVideoProcessorDeviceCaps method","IDXVAHD_Device.GetVideoProcessorDeviceCaps","IDXVAHD_Device::GetVideoProcessorDeviceCaps","dxvahd/IDXVAHD_Device::GetVideoProcessorDeviceCaps","mf.idxvahd_device_getvideoprocessordevicecaps"]
old-location: mf\idxvahd_device_getvideoprocessordevicecaps.htm
tech.root: mf
ms.assetid: 93acad97-feee-46a5-95bf-51e560f91057
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorDeviceCaps, GetVideoProcessorDeviceCaps method [Media Foundation], GetVideoProcessorDeviceCaps method [Media Foundation],IDXVAHD_Device interface, IDXVAHD_Device interface [Media Foundation],GetVideoProcessorDeviceCaps method, IDXVAHD_Device.GetVideoProcessorDeviceCaps, IDXVAHD_Device::GetVideoProcessorDeviceCaps, dxvahd/IDXVAHD_Device::GetVideoProcessorDeviceCaps, mf.idxvahd_device_getvideoprocessordevicecaps
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
 - IDXVAHD_Device::GetVideoProcessorDeviceCaps
 - dxvahd/IDXVAHD_Device::GetVideoProcessorDeviceCaps
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
 - IDXVAHD_Device.GetVideoProcessorDeviceCaps
---

# IDXVAHD_Device::GetVideoProcessorDeviceCaps


## -description

Gets the capabilities of the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -parameters

### -param pCaps [out]

A pointer to a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure that receives the device capabilities.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device">IDXVAHD_Device</a>