---
UID: NS:dxvahd._DXVAHD_BLT_STATE_CONSTRICTION_DATA
title: "_DXVAHD_BLT_STATE_CONSTRICTION_DATA"
author: windows-sdk-content
description: Specifies whether the output is downsampled in a blit operation, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_blt_state_constriction_data.htm
old-project: medfound
ms.assetid: 962a99bd-060d-4101-b65a-d0406e136bf7
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DXVAHD_BLT_STATE_CONSTRICTION_DATA, DXVAHD_BLT_STATE_CONSTRICTION_DATA structure [Media Foundation], _DXVAHD_BLT_STATE_CONSTRICTION_DATA, dxvahd/DXVAHD_BLT_STATE_CONSTRICTION_DATA, mf.dxvahd_blt_state_constriction_data
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
req.typenames: DXVAHD_BLT_STATE_CONSTRICTION_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxvahd.h
api_name:
-	DXVAHD_BLT_STATE_CONSTRICTION_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAHD_BLT_STATE_CONSTRICTION_DATA structure


## -description


Specifies whether the output is downsampled in a  blit operation, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field Enable

If <b>TRUE</b>, downsampling is enabled<b></b>. Otherwise, downsampling is disabled and the <b>Size</b> member is ignored. The default state value is <b>FALSE</b> (downsampling is disabled).


### -field Size

The sampling size. The default value is (1,1).


## -remarks



If the <b>Enable</b> member is <b>TRUE</b>, the device downsamples the composed target rectangle  to the size given in the <b>Size</b> member, and then scales it back to the size of the target rectangle.

The width and height of <b>Size</b> must be greater than zero. If the size is larger than the target rectangle, downsampling does not occur.

To use this state, the device must support downsampling, indicated by the <b>DXVAHD_FEATURE_CAPS_CONSTRICTION</b> capability flag. To query for this capability, call <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>. If the device supports downsampling, it sets the <b>DXVAHD_FEATURE_CAPS_CONSTRICTION</b> flag in the <b>FeatureCaps</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure. 

If the device does not support downsampling, the <a href="https://msdn.microsoft.com/adc08662-7977-402d-9eb1-505333550fc8">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a> method fails for this state.

Downsampling is sometimes used to reduce the quality of premium content when other forms of content protection are not available.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/cd5f56ff-61d7-49df-8114-f6a14de8e06b">DXVAHD_BLT_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/adc08662-7977-402d-9eb1-505333550fc8">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

