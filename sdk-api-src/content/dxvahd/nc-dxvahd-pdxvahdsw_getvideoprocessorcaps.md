---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorCaps
title: PDXVAHDSW_GetVideoProcessorCaps (dxvahd.h)
description: Gets the capabilities of one or more software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processors.
helpviewer_keywords: ["PDXVAHDSW_GetVideoProcessorCaps","PDXVAHDSW_GetVideoProcessorCaps callback","PDXVAHDSW_GetVideoProcessorCaps callback function [Media Foundation]","dxvahd/PDXVAHDSW_GetVideoProcessorCaps","mf.pdxvahdsw_getvideoprocessorcaps"]
old-location: mf\pdxvahdsw_getvideoprocessorcaps.htm
tech.root: mf
ms.assetid: d32fd5e7-b8e8-431f-bc74-b75288ceb01f
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorCaps, PDXVAHDSW_GetVideoProcessorCaps callback, PDXVAHDSW_GetVideoProcessorCaps callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorCaps, mf.pdxvahdsw_getvideoprocessorcaps
f1_keywords:
- dxvahd/PDXVAHDSW_GetVideoProcessorCaps
dev_langs:
- c++
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
- PDXVAHDSW_GetVideoProcessorCaps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDXVAHDSW_GetVideoProcessorCaps callback function


## -description


Gets the capabilities of one or more software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processors.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


### -param *pContentDesc [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc">DXVAHD_CONTENT_DESC</a> structure that describes the video content.


### -param Usage [in]

A member of the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_device_usage">DXVAHD_DEVICE_USAGE</a> enumeration, describing how the video processor will be used.


### -param Count [in]

The number of elements in the <i>pCaps</i> array.


### -param *pCaps [out]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps">DXVAHD_VPCAPS</a> structures. The function fills the structures with the capabilities of the plug-in video processors.




## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcaps">IDXVAHD_Device::GetVideoProcessorCaps</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

