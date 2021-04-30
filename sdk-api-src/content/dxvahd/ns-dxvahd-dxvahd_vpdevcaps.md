---
UID: NS:dxvahd._DXVAHD_VPDEVCAPS
title: DXVAHD_VPDEVCAPS (dxvahd.h)
description: Specifies the capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["DXVAHD_VPDEVCAPS","DXVAHD_VPDEVCAPS structure [Media Foundation]","dxvahd/DXVAHD_VPDEVCAPS","mf.dxvahd_vpdevcaps"]
old-location: mf\dxvahd_vpdevcaps.htm
tech.root: mf
ms.assetid: 340669d4-2a84-4030-83c3-a61469fdfd61
ms.date: 12/05/2018
ms.keywords: DXVAHD_VPDEVCAPS, DXVAHD_VPDEVCAPS structure [Media Foundation], dxvahd/DXVAHD_VPDEVCAPS, mf.dxvahd_vpdevcaps
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
req.typenames: DXVAHD_VPDEVCAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_VPDEVCAPS
 - dxvahd/_DXVAHD_VPDEVCAPS
 - DXVAHD_VPDEVCAPS
 - dxvahd/DXVAHD_VPDEVCAPS
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
 - DXVAHD_VPDEVCAPS
---

# DXVAHD_VPDEVCAPS structure


## -description

Specifies the capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -struct-fields

### -field DeviceType

Specifies the device type, as a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_device_type">DXVAHD_DEVICE_TYPE</a> enumeration.

### -field DeviceCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_device_caps">DXVAHD_DEVICE_CAPS</a> enumeration.

### -field FeatureCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_feature_caps">DXVAHD_FEATURE_CAPS</a> enumeration.

### -field FilterCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_filter_caps">DXVAHD_FILTER_CAPS</a> enumeration.

### -field InputFormatCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_input_format_caps">DXVAHD_INPUT_FORMAT_CAPS</a> enumeration.

### -field InputPool

The memory pool that is required for the input video surfaces.

### -field OutputFormatCount

The number of supported output formats. To get the list of output formats, call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats">IDXVAHD_Device::GetVideoProcessorOutputFormats</a> method.

### -field InputFormatCount

The number of supported input formats. To get the list of input formats, call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats">IDXVAHD_Device::GetVideoProcessorInputFormats</a> method.

### -field VideoProcessorCount

The number of video processors. Each video processor represents a  distinct set of processing capabilities. To get the capabilities of each video processor, call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcaps">IDXVAHD_Device::GetVideoProcessorCaps</a> method. To create a video processor, call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor">IDXVAHD_Device::CreateVideoProcessor</a> method.

### -field MaxInputStreams

The maximum number of input streams that can be enabled at the same time.

### -field MaxStreamStates

The maximum number of input streams for which the device can store state data.

## -remarks

In DXVA-HD, the device stores state information for each input stream. These states persist between blits. With each blit, the application selects which streams to enable or disable. Disabling a stream does not affect the state information for that stream.



The <b>MaxStreamStates</b> member gives the maximum number of stream states that can be set by the application. The <b>MaxInputStreams</b> member gives the maximum number of streams that can be enabled during a blit. These two values can differ.

To set the state data for a stream, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>