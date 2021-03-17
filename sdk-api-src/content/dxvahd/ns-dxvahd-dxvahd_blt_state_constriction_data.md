---
UID: NS:dxvahd._DXVAHD_BLT_STATE_CONSTRICTION_DATA
title: DXVAHD_BLT_STATE_CONSTRICTION_DATA (dxvahd.h)
description: Specifies whether the output is downsampled in a blit operation, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_BLT_STATE_CONSTRICTION_DATA","DXVAHD_BLT_STATE_CONSTRICTION_DATA structure [Media Foundation]","dxvahd/DXVAHD_BLT_STATE_CONSTRICTION_DATA","mf.dxvahd_blt_state_constriction_data"]
old-location: mf\dxvahd_blt_state_constriction_data.htm
tech.root: mf
ms.assetid: 962a99bd-060d-4101-b65a-d0406e136bf7
ms.date: 12/05/2018
ms.keywords: DXVAHD_BLT_STATE_CONSTRICTION_DATA, DXVAHD_BLT_STATE_CONSTRICTION_DATA structure [Media Foundation], dxvahd/DXVAHD_BLT_STATE_CONSTRICTION_DATA, mf.dxvahd_blt_state_constriction_data
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
req.typenames: DXVAHD_BLT_STATE_CONSTRICTION_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_BLT_STATE_CONSTRICTION_DATA
 - dxvahd/_DXVAHD_BLT_STATE_CONSTRICTION_DATA
 - DXVAHD_BLT_STATE_CONSTRICTION_DATA
 - dxvahd/DXVAHD_BLT_STATE_CONSTRICTION_DATA
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
 - DXVAHD_BLT_STATE_CONSTRICTION_DATA
---

# DXVAHD_BLT_STATE_CONSTRICTION_DATA structure


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

To use this state, the device must support downsampling, indicated by the <b>DXVAHD_FEATURE_CAPS_CONSTRICTION</b> capability flag. To query for this capability, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>. If the device supports downsampling, it sets the <b>DXVAHD_FEATURE_CAPS_CONSTRICTION</b> flag in the <b>FeatureCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure. 

If the device does not support downsampling, the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a> method fails for this state.

Downsampling is sometimes used to reduce the quality of premium content when other forms of content protection are not available.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_blt_state">DXVAHD_BLT_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>