---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _DXVAHD_STREAM_STATE enumeration


## -description


Specifies state parameters for an input stream to a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

To set a state parameter, call  <a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>. This method takes a <b>DXVAHD_STREAM_STATE</b> value and a byte array as input.  The byte array contains state data, the structure of which is defined by the <b>DXVAHD_STREAM_STATE</b> value.


## -enum-fields




### -field DXVAHD_STREAM_STATE_D3DFORMAT

Specifies the video format of the input stream. The state data is a  <a href="https://msdn.microsoft.com/a1ba825b-0574-4657-8a10-447a3caf8149">DXVAHD_STREAM_STATE_D3DFORMAT_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FRAME_FORMAT

Specifies how the input stream is interlaced. The state data is a  <a href="https://msdn.microsoft.com/4fa6a7f7-df9f-4e38-884c-81a01f913df0">DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE

Specifies the color space for the input stream. The state data is a <a href="https://msdn.microsoft.com/54b53e4d-990b-4496-aae6-039f443337ae">DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA</a>  structure.


### -field DXVAHD_STREAM_STATE_OUTPUT_RATE

Specifies the output frame rate. The state data is a  <a href="https://msdn.microsoft.com/9cca24f0-5fff-4125-b1fe-d2f9278b5181">DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_SOURCE_RECT

Specifies the source rectangle. The source rectangle defines which portion of the input sample is blitted to the destination surface. The state data is a  <a href="https://msdn.microsoft.com/51f2cfe6-722b-4273-abf6-e1b8fdec9808">DXVAHD_STREAM_STATE_SOURCE_RECT_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_DESTINATION_RECT

Specifies the destination rectangle. The destination rectangle defines which portion of the destination rectangle receives the blit. The state data is a  <a href="https://msdn.microsoft.com/f850531b-eee0-4943-8c41-050ec78eab63">DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_ALPHA

Specifies the planar alpha value for this input stream. The state data is a  <a href="https://msdn.microsoft.com/51135d6e-4f97-44d9-b1d5-f7d2095ee6f1">DXVAHD_STREAM_STATE_ALPHA_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_PALETTE

Specifies the color-palette entries. The state data is a  <a href="https://msdn.microsoft.com/91f69451-72e6-4028-92d5-555dcf834cf7">DXVAHD_STREAM_STATE_PALETTE_DATA</a> structure.

 This setting is used for palettized input formats, such as AI44 and IA44. 


### -field DXVAHD_STREAM_STATE_LUMA_KEY

Specifies the luma key. The state data is a  <a href="https://msdn.microsoft.com/d94b04d9-9d94-4392-a0bf-a33210aeef1f">DXVAHD_STREAM_STATE_LUMA_KEY_DATA</a> structure.

This state is applicable only if the device supports luma keying. To find out if the device supports luma keying, check for the <b>DXVAHD_FEATURE_CAPS_LUMA_KEY</b> flag in the <b>FeatureCaps </b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> capabilities structure. 


### -field DXVAHD_STREAM_STATE_ASPECT_RATIO

Specifies the pixel aspect ratio of the source and destination surfaces. The state data is a  <a href="https://msdn.microsoft.com/dd7ab16e-2dc6-462e-b55d-b93a14c362cf">DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_BRIGHTNESS

Specifies the brightness filter. The state data is a  <a href="https://msdn.microsoft.com/2f70222d-f87a-49a5-8da5-15dfa2807cd7">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_CONTRAST

Specifies the contrast filter. The state data is a  <a href="https://msdn.microsoft.com/2f70222d-f87a-49a5-8da5-15dfa2807cd7">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_HUE

Specifies the hue filter. The state data is a <a href="https://msdn.microsoft.com/2f70222d-f87a-49a5-8da5-15dfa2807cd7">DXVAHD_STREAM_STATE_FILTER_DATA</a>  structure.


### -field DXVAHD_STREAM_STATE_FILTER_SATURATION

Specifies the saturation filter. The state data is a  <a href="https://msdn.microsoft.com/2f70222d-f87a-49a5-8da5-15dfa2807cd7">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_NOISE_REDUCTION

Specifies the noise-reduction filter. The state data is a  <a href="https://msdn.microsoft.com/2f70222d-f87a-49a5-8da5-15dfa2807cd7">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_EDGE_ENHANCEMENT

Specifies the edge-enhancement filter. The state data is a  <a href="https://msdn.microsoft.com/2f70222d-f87a-49a5-8da5-15dfa2807cd7">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_FILTER_ANAMORPHIC_SCALING

Specifies the anamorphic-scaling value. The state data is a  <a href="https://msdn.microsoft.com/2f70222d-f87a-49a5-8da5-15dfa2807cd7">DXVAHD_STREAM_STATE_FILTER_DATA</a> structure.


### -field DXVAHD_STREAM_STATE_PRIVATE

Specifies that the state data contains a private DXVA-HD stream state.  The state data is a  <a href="https://msdn.microsoft.com/3b7ce487-edec-4ff2-b971-72ddcc28162c">DXVAHD_STREAM_STATE_PRIVATE_DATA</a> structure.

Use this state for proprietary or device-specific parameters.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/1ceeae95-d67d-4f11-b815-f4eef517e7ce">IDXVAHD_VideoProcessor::GetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

