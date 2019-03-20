---
UID: NE:dxvahd._DXVAHD_ALPHA_FILL_MODE
title: DXVAHD_ALPHA_FILL_MODE (dxvahd.h)
author: windows-sdk-content
description: Specifies how the output alpha values are calculated for Microsoft DirectX Video Acceleration High Definition (DXVA-HD) blit operations.
old-location: mf\dxvahd_alpha_fill_mode.htm
tech.root: medfound
ms.assetid: f5e9f37e-5600-4139-86b2-7f63c2981b69
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DXVAHD_ALPHA_FILL_MODE, DXVAHD_ALPHA_FILL_MODE enumeration [Media Foundation], DXVAHD_ALPHA_FILL_MODE_BACKGROUND, DXVAHD_ALPHA_FILL_MODE_DESTINATION, DXVAHD_ALPHA_FILL_MODE_OPAQUE, DXVAHD_ALPHA_FILL_MODE_SOURCE_STREAM, dxvahd/DXVAHD_ALPHA_FILL_MODE, dxvahd/DXVAHD_ALPHA_FILL_MODE_BACKGROUND, dxvahd/DXVAHD_ALPHA_FILL_MODE_DESTINATION, dxvahd/DXVAHD_ALPHA_FILL_MODE_OPAQUE, dxvahd/DXVAHD_ALPHA_FILL_MODE_SOURCE_STREAM, mf.dxvahd_alpha_fill_mode
ms.topic: enum
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
 - DXVAHD_ALPHA_FILL_MODE
product: Windows
targetos: Windows
req.typenames: DXVAHD_ALPHA_FILL_MODE
req.redist: 
---

# DXVAHD_ALPHA_FILL_MODE enumeration


## -description


Specifies how the output alpha values are calculated for Microsoft DirectX Video Acceleration High Definition (DXVA-HD) blit operations.


## -enum-fields




### -field DXVAHD_ALPHA_FILL_MODE_OPAQUE

Alpha values inside the target rectangle are set to opaque.


### -field DXVAHD_ALPHA_FILL_MODE_BACKGROUND

Alpha values inside the target rectangle are set to the alpha value specified in the background color. See <a href="https://msdn.microsoft.com/en-us/library/Dd318392(v=VS.85).aspx">DXVAHD_BLT_STATE_BACKGROUND_COLOR</a>.


### -field DXVAHD_ALPHA_FILL_MODE_DESTINATION

Existing alpha values remain unchanged in the output surface.


### -field DXVAHD_ALPHA_FILL_MODE_SOURCE_STREAM

Alpha values from the input stream  are scaled and copied to the corresponding destination rectangle for that stream. If the input stream does not have alpha data, the DXVA-HD device sets the alpha values in the target rectangle to an opaque value. If the input stream is disabled or the source rectangle is empty, the alpha values in the target rectangle are not modified.


## -remarks



The <b>Mode</b> member of the <a href="https://msdn.microsoft.com/dcd42210-d5f8-42c7-aac0-08f0ce4b7ac9">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a> structure has this enumeration type. That member specifies the alpha-fill mode for the input stream identified by the <b>StreamNumber</b> member of the same structure. To set the alpha-fill mode, call  <a href="https://msdn.microsoft.com/adc08662-7977-402d-9eb1-505333550fc8">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>.

To find out which modes the device supports, call the <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> method. If the device sets the <b>DXVAHD_FEATURE_CAPS_ALPHA_FILL</b> flag in the <b>FeatureCaps</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure, the DXVA-HD device supports any of the modes listed here. Otherwise, the alpha-fill mode must be <b>DXVAHD_ALPHA_FILL_MODE_OPAQUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/dcd42210-d5f8-42c7-aac0-08f0ce4b7ac9">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

