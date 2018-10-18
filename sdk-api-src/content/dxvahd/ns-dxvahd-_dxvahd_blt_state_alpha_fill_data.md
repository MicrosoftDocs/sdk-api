---
UID: NS:dxvahd._DXVAHD_BLT_STATE_ALPHA_FILL_DATA
title: "_DXVAHD_BLT_STATE_ALPHA_FILL_DATA"
author: windows-sdk-content
description: Specifies how the output alpha values are calculated for blit operations when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_blt_state_alpha_fill_data.htm
tech.root: medfound
ms.assetid: dcd42210-d5f8-42c7-aac0-08f0ce4b7ac9
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: DXVAHD_BLT_STATE_ALPHA_FILL_DATA, DXVAHD_BLT_STATE_ALPHA_FILL_DATA structure [Media Foundation], _DXVAHD_BLT_STATE_ALPHA_FILL_DATA, dxvahd/DXVAHD_BLT_STATE_ALPHA_FILL_DATA, mf.dxvahd_blt_state_alpha_fill_data
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - DXVAHD_BLT_STATE_ALPHA_FILL_DATA
product: Windows
targetos: Windows
req.typenames: DXVAHD_BLT_STATE_ALPHA_FILL_DATA
req.redist: 
---

# _DXVAHD_BLT_STATE_ALPHA_FILL_DATA structure


## -description


Specifies how the output alpha values are calculated for blit operations when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field Mode

Specifies the alpha fill mode, as a member of the <a href="https://msdn.microsoft.com/f5e9f37e-5600-4139-86b2-7f63c2981b69">DXVAHD_ALPHA_FILL_MODE</a> enumeration.

If the <b>FeatureCaps</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure does not contain the <b>DXVAHD_FEATURE_CAPS_ALPHA_FILL</b> flag, the alpha fill mode must be set to <b>DXVAHD_ALPHA_FILL_MODE_OPAQUE</b>.

The default state value is <b>DXVAHD_ALPHA_FILL_MODE_OPAQUE</b>.


### -field StreamNumber

Zero-based index of the input stream to use for the alpha values. This member is used when the alpha fill mode is <b>DXVAHD_ALPHA_FILL_MODE_SOURCE_STREAM</b>; otherwise, the value is ignored. 

To get the maximum number of streams, call <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>MaxStreamStates</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/cd5f56ff-61d7-49df-8114-f6a14de8e06b">DXVAHD_BLT_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/adc08662-7977-402d-9eb1-505333550fc8">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

