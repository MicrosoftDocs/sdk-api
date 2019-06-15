---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorDeviceCaps
title: PDXVAHDSW_GetVideoProcessorDeviceCaps (dxvahd.h)
author: windows-sdk-content
description: Gets the capabilities of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\pdxvahdsw_getvideoprocessordevicecaps.htm
tech.root: medfound
ms.assetid: 09753e3b-7235-4204-ad08-a083a7db4a2b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorDeviceCaps, PDXVAHDSW_GetVideoProcessorDeviceCaps callback, PDXVAHDSW_GetVideoProcessorDeviceCaps callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorDeviceCaps, mf.pdxvahdsw_getvideoprocessordevicecaps
ms.topic: callback
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
 - UserDefined
api_location:
 - dxvahd.h
api_name:
 - PDXVAHDSW_GetVideoProcessorDeviceCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDXVAHDSW_GetVideoProcessorDeviceCaps callback function


## -description


Gets the capabilities of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


### -param *pContentDesc [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_content_desc">DXVAHD_CONTENT_DESC</a> structure that describes the video content.


### -param Usage [in]

A member of the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ne-dxvahd-_dxvahd_device_usage">DXVAHD_DEVICE_USAGE</a> enumeration, describing how the device will be used. The value indicates the desired trade-off between speed and video quality.


### -param *pCaps [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure that receives the device capabilities.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

