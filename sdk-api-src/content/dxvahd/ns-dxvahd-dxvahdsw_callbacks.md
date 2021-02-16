---
UID: NS:dxvahd._DXVAHDSW_CALLBACKS
title: DXVAHDSW_CALLBACKS (dxvahd.h)
description: Contains pointers to functions implemented by a software plug-in for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHDSW_CALLBACKS","DXVAHDSW_CALLBACKS structure [Media Foundation]","dxvahd/DXVAHDSW_CALLBACKS","mf.dxvahdsw_callbacks"]
old-location: mf\dxvahdsw_callbacks.htm
tech.root: mf
ms.assetid: 74c329cc-af54-4cf8-8cb6-eed9e96db4c5
ms.date: 12/05/2018
ms.keywords: DXVAHDSW_CALLBACKS, DXVAHDSW_CALLBACKS structure [Media Foundation], dxvahd/DXVAHDSW_CALLBACKS, mf.dxvahdsw_callbacks
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
req.typenames: DXVAHDSW_CALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHDSW_CALLBACKS
 - dxvahd/_DXVAHDSW_CALLBACKS
 - DXVAHDSW_CALLBACKS
 - dxvahd/DXVAHDSW_CALLBACKS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHDSW_CALLBACKS
---

# DXVAHDSW_CALLBACKS structure


## -description

Contains pointers to functions implemented by a software plug-in for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

## -struct-fields

### -field CreateDevice

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_createdevice">PDXVAHDSW_CreateDevice</a>.

### -field ProposeVideoPrivateFormat

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_proposevideoprivateformat">PDXVAHDSW_ProposeVideoPrivateFormat</a>.

### -field GetVideoProcessorDeviceCaps

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_getvideoprocessordevicecaps">PDXVAHDSW_GetVideoProcessorDeviceCaps</a>.

### -field GetVideoProcessorOutputFormats

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_getvideoprocessoroutputformats">PDXVAHDSW_GetVideoProcessorOutputFormats</a>.

### -field GetVideoProcessorInputFormats

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_getvideoprocessorinputformats">PDXVAHDSW_GetVideoProcessorInputFormats</a>.

### -field GetVideoProcessorCaps

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_getvideoprocessorcaps">PDXVAHDSW_GetVideoProcessorCaps</a>.

### -field GetVideoProcessorCustomRates

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_getvideoprocessorcustomrates">PDXVAHDSW_GetVideoProcessorCustomRates</a>.

### -field GetVideoProcessorFilterRange

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_getvideoprocessorfilterrange">PDXVAHDSW_GetVideoProcessorFilterRange</a>.

### -field DestroyDevice

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_destroydevice">PDXVAHDSW_DestroyDevice</a>.

### -field CreateVideoProcessor

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_createvideoprocessor">PDXVAHDSW_CreateVideoProcessor</a>.

### -field SetVideoProcessBltState

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_setvideoprocessbltstate">PDXVAHDSW_SetVideoProcessBltState</a>.

### -field GetVideoProcessBltStatePrivate

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_getvideoprocessbltstateprivate">PDXVAHDSW_GetVideoProcessBltStatePrivate</a>.

### -field SetVideoProcessStreamState

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_setvideoprocessstreamstate">PDXVAHDSW_SetVideoProcessStreamState</a>.

### -field GetVideoProcessStreamStatePrivate

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_getvideoprocessstreamstateprivate">PDXVAHDSW_GetVideoProcessStreamStatePrivate</a>.

### -field VideoProcessBltHD

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_videoprocessblthd">PDXVAHDSW_VideoProcessBltHD</a>.

### -field DestroyVideoProcessor

Function pointer of type <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_destroyvideoprocessor">PDXVAHDSW_DestroyVideoProcessor</a>.

## -remarks

If you provide a software plug-in for DXVA-HD, the plug-in must implement a set of functions that are defined by the function pointer types in this structure.

At initialization, the   DXVA-HD runtime calls the plug-in device's <a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_plugin">PDXVAHDSW_Plugin</a> function. This function fills in a <b>DXVAHDSW_CALLBACKS</b> structure with pointers to  the set of functions that are implemented by the plug-in device. When the application calls DXVA-HD methods, the DXVA-HD runtime calls the corresponding plug-in functions.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/api/dxvahd/nc-dxvahd-pdxvahdsw_plugin">PDXVAHDSW_Plugin</a>