---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorFilterRange
title: PDXVAHDSW_GetVideoProcessorFilterRange (dxvahd.h)
description: Gets the supported range of image filter values from a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["PDXVAHDSW_GetVideoProcessorFilterRange","PDXVAHDSW_GetVideoProcessorFilterRange callback","PDXVAHDSW_GetVideoProcessorFilterRange callback function [Media Foundation]","dxvahd/PDXVAHDSW_GetVideoProcessorFilterRange","mf.pdxvahdsw_getvideoprocessorfilterrange"]
old-location: mf\pdxvahdsw_getvideoprocessorfilterrange.htm
tech.root: mf
ms.assetid: 3c28ffcf-dad5-4ed1-8b04-12e22fd566a4
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorFilterRange, PDXVAHDSW_GetVideoProcessorFilterRange callback, PDXVAHDSW_GetVideoProcessorFilterRange callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorFilterRange, mf.pdxvahdsw_getvideoprocessorfilterrange
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
 - PDXVAHDSW_GetVideoProcessorFilterRange
 - dxvahd/PDXVAHDSW_GetVideoProcessorFilterRange
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
 - PDXVAHDSW_GetVideoProcessorFilterRange
---

# PDXVAHDSW_GetVideoProcessorFilterRange callback function


## -description

Gets the supported range of image filter values from a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -parameters

### -param hDevice [in]

A handle to the plug-in DXVA-HD device.

### -param Filter [in]

The type of image filter, specified as a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_filter">DXVAHD_FILTER</a> enumeration.

### -param pRange [out]

A pointer to a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_filter_range_data">DXVAHD_FILTER_RANGE_DATA</a> structure. The function fills the structure with the range of values for the specified filter.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorfilterrange">IDXVAHD_Device::GetVideoProcessorFilterRange</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
