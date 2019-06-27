---
UID: NE:dxvahd._DXVAHD_BLT_STATE
title: DXVAHD_BLT_STATE (dxvahd.h)
author: windows-sdk-content
description: Specifies state parameters for blit operations when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_blt_state.htm
tech.root: medfound
ms.assetid: cd5f56ff-61d7-49df-8114-f6a14de8e06b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DXVAHD_BLT_STATE, DXVAHD_BLT_STATE enumeration [Media Foundation], DXVAHD_BLT_STATE_ALPHA_FILL, DXVAHD_BLT_STATE_BACKGROUND_COLOR, DXVAHD_BLT_STATE_CONSTRICTION, DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE, DXVAHD_BLT_STATE_PRIVATE, DXVAHD_BLT_STATE_TARGET_RECT, dxvahd/DXVAHD_BLT_STATE, dxvahd/DXVAHD_BLT_STATE_ALPHA_FILL, dxvahd/DXVAHD_BLT_STATE_BACKGROUND_COLOR, dxvahd/DXVAHD_BLT_STATE_CONSTRICTION, dxvahd/DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE, dxvahd/DXVAHD_BLT_STATE_PRIVATE, dxvahd/DXVAHD_BLT_STATE_TARGET_RECT, mf.dxvahd_blt_state
ms.topic: enum
f1_keywords: 
 - "dxvahd/DXVAHD_BLT_STATE"
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
 - DXVAHD_BLT_STATE
product: Windows
targetos: Windows
req.typenames: DXVAHD_BLT_STATE
req.redist: 
ms.custom: 19H1
---

# DXVAHD_BLT_STATE enumeration


## -description


Specifies state parameters for blit operations when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

To set a state parameter, call the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a> method. This method takes a <b>DXVAHD_BLT_STATE</b> value and a byte array as input.  The byte array contains state data, the structure of which is defined by the <b>DXVAHD_BLT_STATE</b> value.


## -enum-fields




### -field DXVAHD_BLT_STATE_TARGET_RECT

Specifies the target rectangle, which is the area within the destination surface where the output will be drawn. The state data is a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_blt_state_target_rect_data">DXVAHD_BLT_STATE_TARGET_RECT_DATA</a> structure.


### -field DXVAHD_BLT_STATE_BACKGROUND_COLOR

Specifies the background color. The state data is a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_blt_state_background_color_data">DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA</a> structure.


### -field DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE

Specifies the output color space.  The state data is a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_blt_state_output_color_space_data">DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA</a> structure.


### -field DXVAHD_BLT_STATE_ALPHA_FILL

Specifies how DXVA-HD device calculates output alpha values.  The state data is a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_blt_state_alpha_fill_data">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a> structure.


### -field DXVAHD_BLT_STATE_CONSTRICTION

Specifies the amount of downsampling to perform on the output.  The state data is a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_blt_state_constriction_data">DXVAHD_BLT_STATE_CONSTRICTION_DATA</a> structure.


### -field DXVAHD_BLT_STATE_PRIVATE

Specifies that the state data contains a private DXVA-HD blit state.  Use this state for proprietary or device-specific parameters. The state data is a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahd_blt_state_private_data">DXVAHD_BLT_STATE_PRIVATE_DATA</a>  structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

