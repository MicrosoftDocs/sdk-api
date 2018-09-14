---
UID: NE:dxvahd._DXVAHD_PROCESSOR_CAPS
title: "_DXVAHD_PROCESSOR_CAPS"
author: windows-sdk-content
description: Specifies the processing capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\dxvahd_processor_caps.htm
tech.root: medfound
ms.assetid: 6fe6b1fe-4eef-427a-b28f-a359b066e552
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: DXVAHD_PROCESSOR_CAPS, DXVAHD_PROCESSOR_CAPS enumeration [Media Foundation], DXVAHD_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE, DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BLEND, DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BOB, DXVAHD_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION, DXVAHD_PROCESSOR_CAPS_FRAME_RATE_CONVERSION, DXVAHD_PROCESSOR_CAPS_INVERSE_TELECINE, _DXVAHD_PROCESSOR_CAPS, dxvahd/DXVAHD_PROCESSOR_CAPS, dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE, dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BLEND, dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BOB, dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION, dxvahd/DXVAHD_PROCESSOR_CAPS_FRAME_RATE_CONVERSION, dxvahd/DXVAHD_PROCESSOR_CAPS_INVERSE_TELECINE, mf.dxvahd_processor_caps
ms.prod: windows
ms.technology: windows-sdk
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
 - DXVAHD_PROCESSOR_CAPS
product: Windows
targetos: Windows
req.typenames: DXVAHD_PROCESSOR_CAPS
req.redist: 
---

# _DXVAHD_PROCESSOR_CAPS enumeration


## -description


Specifies the processing capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -enum-fields




### -field DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BLEND

The video processor can perform blend deinterlacing.

 In <i>blend deinterlacing</i>, the two fields from an interlaced frame are blended into a single progressive frame. A video processor uses blend deinterlacing when it deinterlaces at half rate, as when converting 60i to 30p. Blend deinterlacing does not require reference frames.


### -field DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BOB

The video processor can perform bob deinterlacing. 

In <i>bob deinterlacing</i>, missing field lines are interpolated from the lines above and below. Bob deinterlacing does not require reference frames.


### -field DXVAHD_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE

The video processor can perform adaptive deinterlacing.

<i>Adaptive deinterlacing</i> uses spatial or temporal interpolation, and switches between the two on a field-by-field basis, depending on the amount of motion. If the video processor does not receive enough reference frames to perform adaptive deinterlacing, it falls back to bob deinterlacing.


### -field DXVAHD_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION

The video processor  can perform motion-compensated deinterlacing.

<i>Motion-compensated deinterlacing</i> uses motion vectors to recreate missing lines. If the video processor does not receive enough reference frames to perform motion-compensated deinterlacing, it falls back to bob deinterlacing.


### -field DXVAHD_PROCESSOR_CAPS_INVERSE_TELECINE

The video processor can perform inverse telecine (IVTC).

 If the video processor supports this capability, the <b>ITelecineCaps</b> member of the <a href="https://msdn.microsoft.com/25ec6802-ca6e-42d4-b1d5-de7597e3d042">DXVAHD_VPCAPS</a> structure specifies which IVTC modes are supported.


### -field DXVAHD_PROCESSOR_CAPS_FRAME_RATE_CONVERSION

The video processor can convert the frame rate by interpolating frames.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

