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

# _DXVAHD_BLT_STATE enumeration


## -description


Specifies state parameters for blit operations when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

To set a state parameter, call the <a href="https://msdn.microsoft.com/adc08662-7977-402d-9eb1-505333550fc8">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a> method. This method takes a <b>DXVAHD_BLT_STATE</b> value and a byte array as input.  The byte array contains state data, the structure of which is defined by the <b>DXVAHD_BLT_STATE</b> value.


## -enum-fields




### -field DXVAHD_BLT_STATE_TARGET_RECT

Specifies the target rectangle, which is the area within the destination surface where the output will be drawn. The state data is a <a href="https://msdn.microsoft.com/2a810071-b5f7-4216-8108-83dce5c12836">DXVAHD_BLT_STATE_TARGET_RECT_DATA</a> structure.


### -field DXVAHD_BLT_STATE_BACKGROUND_COLOR

Specifies the background color. The state data is a <a href="https://msdn.microsoft.com/34b8c29e-a183-4e68-bd46-802c43d554f7">DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA</a> structure.


### -field DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE

Specifies the output color space.  The state data is a <a href="https://msdn.microsoft.com/ec817ebc-dc3f-4101-863a-218f0a8c998a">DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA</a> structure.


### -field DXVAHD_BLT_STATE_ALPHA_FILL

Specifies how DXVA-HD device calculates output alpha values.  The state data is a <a href="https://msdn.microsoft.com/dcd42210-d5f8-42c7-aac0-08f0ce4b7ac9">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a> structure.


### -field DXVAHD_BLT_STATE_CONSTRICTION

Specifies the amount of downsampling to perform on the output.  The state data is a <a href="https://msdn.microsoft.com/962a99bd-060d-4101-b65a-d0406e136bf7">DXVAHD_BLT_STATE_CONSTRICTION_DATA</a> structure.


### -field DXVAHD_BLT_STATE_PRIVATE

Specifies that the state data contains a private DXVA-HD blit state.  Use this state for proprietary or device-specific parameters. The state data is a <a href="https://msdn.microsoft.com/b85d4429-9346-4c85-8c3d-efffe0c1e63a">DXVAHD_BLT_STATE_PRIVATE_DATA</a>  structure.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

