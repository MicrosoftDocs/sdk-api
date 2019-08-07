---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorOutputFormats
title: PDXVAHDSW_GetVideoProcessorOutputFormats (dxvahd.h)
author: windows-sdk-content
description: Gets the output formats that are supported by a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\pdxvahdsw_getvideoprocessoroutputformats.htm
tech.root: medfound
ms.assetid: d7f767d2-c645-4ade-9b0c-0d5436cf0cfe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorOutputFormats, PDXVAHDSW_GetVideoProcessorOutputFormats callback, PDXVAHDSW_GetVideoProcessorOutputFormats callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorOutputFormats, mf.pdxvahdsw_getvideoprocessoroutputformats
ms.topic: callback
f1_keywords:
- dxvahd/PDXVAHDSW_GetVideoProcessorOutputFormats
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
- PDXVAHDSW_GetVideoProcessorOutputFormats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDXVAHDSW_GetVideoProcessorOutputFormats callback function


## -description


Gets the output formats that are supported by a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


### -param *pContentDesc [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc">DXVAHD_CONTENT_DESC</a> structure that describes the video content.


### -param Usage [in]

A member of the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_device_usage">DXVAHD_DEVICE_USAGE</a> enumeration, describing how the device will be used.


### -param Count [in]

The number of formats to retrieve.


### -param *pFormats [out]

A pointer to an array of <b>D3DFORMAT</b> values. The <i>Count</i> parameter specifies the number of elements in the array. The function fills the array with a list of output formats.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats">IDXVAHD_Device::GetVideoProcessorOutputFormats</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

