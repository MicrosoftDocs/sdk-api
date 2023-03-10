---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorDeviceCaps
title: PDXVAHDSW_GetVideoProcessorDeviceCaps (dxvahd.h)
description: Gets the capabilities of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["PDXVAHDSW_GetVideoProcessorDeviceCaps","PDXVAHDSW_GetVideoProcessorDeviceCaps callback","PDXVAHDSW_GetVideoProcessorDeviceCaps callback function [Media Foundation]","dxvahd/PDXVAHDSW_GetVideoProcessorDeviceCaps","mf.pdxvahdsw_getvideoprocessordevicecaps"]
old-location: mf\pdxvahdsw_getvideoprocessordevicecaps.htm
tech.root: mf
ms.assetid: 09753e3b-7235-4204-ad08-a083a7db4a2b
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorDeviceCaps, PDXVAHDSW_GetVideoProcessorDeviceCaps callback, PDXVAHDSW_GetVideoProcessorDeviceCaps callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorDeviceCaps, mf.pdxvahdsw_getvideoprocessordevicecaps
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
 - PDXVAHDSW_GetVideoProcessorDeviceCaps
 - dxvahd/PDXVAHDSW_GetVideoProcessorDeviceCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxvahd.h
api_name:
 - PDXVAHDSW_GetVideoProcessorDeviceCaps
---

# PDXVAHDSW_GetVideoProcessorDeviceCaps callback function


## -description

Gets the capabilities of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -parameters

### -param hDevice [in]

A handle to the plug-in DXVA-HD device.

### -param pContentDesc [in]

A pointer to a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc">DXVAHD_CONTENT_DESC</a> structure that describes the video content.

### -param Usage [in]

A member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_device_usage">DXVAHD_DEVICE_USAGE</a> enumeration, describing how the device will be used. The value indicates the desired trade-off between speed and video quality.

### -param pCaps [out]

A pointer to a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure that receives the device capabilities.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
