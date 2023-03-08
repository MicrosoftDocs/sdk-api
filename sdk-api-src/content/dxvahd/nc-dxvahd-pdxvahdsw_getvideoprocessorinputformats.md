---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorInputFormats
title: PDXVAHDSW_GetVideoProcessorInputFormats (dxvahd.h)
description: Gets the input formats that are supported by a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["PDXVAHDSW_GetVideoProcessorInputFormats","PDXVAHDSW_GetVideoProcessorInputFormats callback","PDXVAHDSW_GetVideoProcessorInputFormats callback function [Media Foundation]","dxvahd/PDXVAHDSW_GetVideoProcessorInputFormats","mf.pdxvahdsw_getvideoprocessorinputformats"]
old-location: mf\pdxvahdsw_getvideoprocessorinputformats.htm
tech.root: mf
ms.assetid: 3d24da29-0fdb-4084-9810-1a0c9b04768b
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorInputFormats, PDXVAHDSW_GetVideoProcessorInputFormats callback, PDXVAHDSW_GetVideoProcessorInputFormats callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorInputFormats, mf.pdxvahdsw_getvideoprocessorinputformats
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
 - PDXVAHDSW_GetVideoProcessorInputFormats
 - dxvahd/PDXVAHDSW_GetVideoProcessorInputFormats
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
 - PDXVAHDSW_GetVideoProcessorInputFormats
---

# PDXVAHDSW_GetVideoProcessorInputFormats callback function


## -description

Gets the input formats that are supported by a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -parameters

### -param hDevice [in]

A handle to the plug-in DXVA-HD device.

### -param pContentDesc [in]

A pointer to a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc">DXVAHD_CONTENT_DESC</a> structure that describes the video content.

### -param Usage [in]

A member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_device_usage">DXVAHD_DEVICE_USAGE</a> enumeration, describing how the device will be used.

### -param Count [in]

The number of formats to retrieve.

### -param pFormats [out]

A pointer to an array of <b>D3DFORMAT</b> values. The <i>Count</i> parameter specifies the number of elements in the array. The method fills the array with a list of input formats.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats">IDXVAHD_Device::GetVideoProcessorInputFormats</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
