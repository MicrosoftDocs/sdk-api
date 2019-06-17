---
UID: NE:dxvahd._DXVAHD_STREAM_STATE
title: DXVAHD_STREAM_STATE (dxvahd.h)
author: windows-sdk-content
description: Specifies state parameters for an input stream to a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\dxvahd_stream_state.htm
tech.root: medfound
ms.assetid: 75036101-7498-4d66-afc3-df76ae3cca39
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE, DXVAHD_STREAM_STATE enumeration [Media Foundation], DXVAHD_STREAM_STATE_ALPHA, DXVAHD_STREAM_STATE_ASPECT_RATIO, DXVAHD_STREAM_STATE_D3DFORMAT, DXVAHD_STREAM_STATE_DESTINATION_RECT, DXVAHD_STREAM_STATE_FILTER_ANAMORPHIC_SCALING, DXVAHD_STREAM_STATE_FILTER_BRIGHTNESS, DXVAHD_STREAM_STATE_FILTER_CONTRAST, DXVAHD_STREAM_STATE_FILTER_EDGE_ENHANCEMENT, DXVAHD_STREAM_STATE_FILTER_HUE, DXVAHD_STREAM_STATE_FILTER_NOISE_REDUCTION, DXVAHD_STREAM_STATE_FILTER_SATURATION, DXVAHD_STREAM_STATE_FRAME_FORMAT, DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE, DXVAHD_STREAM_STATE_LUMA_KEY, DXVAHD_STREAM_STATE_OUTPUT_RATE, DXVAHD_STREAM_STATE_PALETTE, DXVAHD_STREAM_STATE_PRIVATE, DXVAHD_STREAM_STATE_SOURCE_RECT, dxvahd/DXVAHD_STREAM_STATE, dxvahd/DXVAHD_STREAM_STATE_ALPHA, dxvahd/DXVAHD_STREAM_STATE_ASPECT_RATIO, dxvahd/DXVAHD_STREAM_STATE_D3DFORMAT, dxvahd/DXVAHD_STREAM_STATE_DESTINATION_RECT, dxvahd/DXVAHD_STREAM_STATE_FILTER_ANAMORPHIC_SCALING, dxvahd/DXVAHD_STREAM_STATE_FILTER_BRIGHTNESS, dxvahd/DXVAHD_STREAM_STATE_FILTER_CONTRAST, dxvahd/DXVAHD_STREAM_STATE_FILTER_EDGE_ENHANCEMENT, dxvahd/DXVAHD_STREAM_STATE_FILTER_HUE, dxvahd/DXVAHD_STREAM_STATE_FILTER_NOISE_REDUCTION, dxvahd/DXVAHD_STREAM_STATE_FILTER_SATURATION, dxvahd/DXVAHD_STREAM_STATE_FRAME_FORMAT, dxvahd/DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE, dxvahd/DXVAHD_STREAM_STATE_LUMA_KEY, dxvahd/DXVAHD_STREAM_STATE_OUTPUT_RATE, dxvahd/DXVAHD_STREAM_STATE_PALETTE, dxvahd/DXVAHD_STREAM_STATE_PRIVATE, dxvahd/DXVAHD_STREAM_STATE_SOURCE_RECT, mf.dxvahd_stream_state
ms.topic: enum
f1_keywords: ["dxvahd/DXVAHD_STREAM_STATE"]
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
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_STREAM_STATE
product: Windows
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE
req.redist: 
ms.custom: 19H1
---

# DXVAHD_STREAM_STATE enumeration


## -description


Specifies state parameters for an input stream to a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

To set a state parameter, call  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>. This method takes a <b>DXVAHD_STREAM_STATE</b> value and a byte array as input.  The byte array contains state data, the structure of which is defined by the <b>DXVAHD_STREAM_STATE</b> value.


## -enum-fields




### -field DXVAHD_STREAM_STATE_D3DFORMAT

Specifies the video format of the input stream. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_d3dformat_data">DXVAHD_STREAM_STATE_D3DFORMAT_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FRAME_FORMAT

Specifies how the input stream is interlaced. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_frame_format_data">DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE

Specifies the color space for the input stream. The state data is a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_input_color_space_data">DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA</a>  structure.


### -field DXVAHD_STREAM_STATE_OUTPUT_RATE

Specifies the output frame rate. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_output_rate_data">DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_SOURCE_RECT

Specifies the source rectangle. The source rectangle defines which portion of the input sample is blitted to the destination surface. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_source_rect_data">DXVAHD_STREAM_STATE_SOURCE_RECT_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_DESTINATION_RECT

Specifies the destination rectangle. The destination rectangle defines which portion of the destination rectangle receives the blit. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_destination_rect_data">DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_ALPHA

Specifies the planar alpha value for this input stream. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_alpha_data">DXVAHD_STREAM_STATE_ALPHA_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_PALETTE

Specifies the color-palette entries. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_palette_data">DXVAHD_STREAM_STATE_PALETTE_DATA</a> structure.

 This setting is used for palettized input formats, such as AI44 and IA44. 


### -field DXVAHD_STREAM_STATE_LUMA_KEY

Specifies the luma key. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_luma_key_data">DXVAHD_STREAM_STATE_LUMA_KEY_DATA</a> structure.

This state is applicable only if the device supports luma keying. To find out if the device supports luma keying, check for the <b>DXVAHD_FEATURE_CAPS_LUMA_KEY</b> flag in the <b>FeatureCaps </b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> capabilities structure. 


### -field DXVAHD_STREAM_STATE_ASPECT_RATIO

Specifies the pixel aspect ratio of the source and destination surfaces. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_aspect_ratio_data">DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_BRIGHTNESS

Specifies the brightness filter. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_filter_data">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_CONTRAST

Specifies the contrast filter. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_filter_data">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_HUE

Specifies the hue filter. The state data is a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_filter_data">DXVAHD_STREAM_STATE_FILTER_DATA</a>  structure.


### -field DXVAHD_STREAM_STATE_FILTER_SATURATION

Specifies the saturation filter. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_filter_data">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_NOISE_REDUCTION

Specifies the noise-reduction filter. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_filter_data">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_EDGE_ENHANCEMENT

Specifies the edge-enhancement filter. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_filter_data">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_ANAMORPHIC_SCALING

Specifies the anamorphic-scaling value. The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_filter_data">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_PRIVATE

Specifies that the state data contains a private DXVA-HD stream state.  The state data is a  <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_stream_state_private_data">DXVAHD_STREAM_STATE_PRIVATE_DATA</a> structure.

Use this state for proprietary or device-specific parameters.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-getvideoprocessstreamstate">IDXVAHD_VideoProcessor::GetVideoProcessStreamState</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

