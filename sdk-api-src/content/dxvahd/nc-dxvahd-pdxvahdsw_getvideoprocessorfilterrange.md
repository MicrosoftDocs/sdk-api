---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorFilterRange
title: PDXVAHDSW_GetVideoProcessorFilterRange (dxvahd.h)
author: windows-sdk-content
description: Gets the supported range of image filter values from a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\pdxvahdsw_getvideoprocessorfilterrange.htm
tech.root: medfound
ms.assetid: 3c28ffcf-dad5-4ed1-8b04-12e22fd566a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorFilterRange, PDXVAHDSW_GetVideoProcessorFilterRange callback, PDXVAHDSW_GetVideoProcessorFilterRange callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorFilterRange, mf.pdxvahdsw_getvideoprocessorfilterrange
ms.topic: callback
f1_keywords: ["dxvahd/PDXVAHDSW_GetVideoProcessorFilterRange"]
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
 - PDXVAHDSW_GetVideoProcessorFilterRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDXVAHDSW_GetVideoProcessorFilterRange callback function


## -description


Gets the supported range of image filter values from a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


### -param Filter [in]

The type of image filter, specified as a member of the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ne-dxvahd-_dxvahd_filter">DXVAHD_FILTER</a> enumeration.


### -param *pRange [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_filter_range_data">DXVAHD_FILTER_RANGE_DATA</a> structure. The function fills the structure with the range of values for the specified filter.




## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorfilterrange">IDXVAHD_Device::GetVideoProcessorFilterRange</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

