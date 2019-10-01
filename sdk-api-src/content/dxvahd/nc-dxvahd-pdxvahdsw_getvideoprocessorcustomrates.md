---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorCustomRates
title: PDXVAHDSW_GetVideoProcessorCustomRates (dxvahd.h)
author: windows-sdk-content
description: Gets the custom rates that a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor supports.
old-location: mf\pdxvahdsw_getvideoprocessorcustomrates.htm
tech.root: medfound
ms.assetid: 0b633dcc-c6eb-47e5-b43b-b2a6cb66abf6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorCustomRates, PDXVAHDSW_GetVideoProcessorCustomRates callback, PDXVAHDSW_GetVideoProcessorCustomRates callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorCustomRates, mf.pdxvahdsw_getvideoprocessorcustomrates
ms.topic: callback
f1_keywords:
- dxvahd/PDXVAHDSW_GetVideoProcessorCustomRates
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
- PDXVAHDSW_GetVideoProcessorCustomRates
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDXVAHDSW_GetVideoProcessorCustomRates callback function


## -description


Gets the custom rates that a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor supports.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


### -param *pVPGuid [in]

A GUID that identifies the video processor to query.


### -param Count [in]

The number of rates to retrieve.


### -param *pRates [out]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_custom_rate_data">DXVAHD_CUSTOM_RATE_DATA</a> structures. The <i>Count</i> parameter specifies the number of elements in the array. The function fills the array with a list of custom rates.




## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcustomrates">IDXVAHD_Device::GetVideoProcessorCustomRates</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

