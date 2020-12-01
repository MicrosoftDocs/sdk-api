---
UID: NS:dxvahd._DXVAHD_BLT_STATE_ALPHA_FILL_DATA
title: DXVAHD_BLT_STATE_ALPHA_FILL_DATA (dxvahd.h)
description: Specifies how the output alpha values are calculated for blit operations when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_BLT_STATE_ALPHA_FILL_DATA","DXVAHD_BLT_STATE_ALPHA_FILL_DATA structure [Media Foundation]","dxvahd/DXVAHD_BLT_STATE_ALPHA_FILL_DATA","mf.dxvahd_blt_state_alpha_fill_data"]
old-location: mf\dxvahd_blt_state_alpha_fill_data.htm
tech.root: mf
ms.assetid: dcd42210-d5f8-42c7-aac0-08f0ce4b7ac9
ms.date: 12/05/2018
ms.keywords: DXVAHD_BLT_STATE_ALPHA_FILL_DATA, DXVAHD_BLT_STATE_ALPHA_FILL_DATA structure [Media Foundation], dxvahd/DXVAHD_BLT_STATE_ALPHA_FILL_DATA, mf.dxvahd_blt_state_alpha_fill_data
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
req.typenames: DXVAHD_BLT_STATE_ALPHA_FILL_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_BLT_STATE_ALPHA_FILL_DATA
 - dxvahd/_DXVAHD_BLT_STATE_ALPHA_FILL_DATA
 - DXVAHD_BLT_STATE_ALPHA_FILL_DATA
 - dxvahd/DXVAHD_BLT_STATE_ALPHA_FILL_DATA
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
 - DXVAHD_BLT_STATE_ALPHA_FILL_DATA
---

# DXVAHD_BLT_STATE_ALPHA_FILL_DATA structure


## -description

Specifies how the output alpha values are calculated for blit operations when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

## -struct-fields

### -field Mode

Specifies the alpha fill mode, as a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_alpha_fill_mode">DXVAHD_ALPHA_FILL_MODE</a> enumeration.

If the <b>FeatureCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure does not contain the <b>DXVAHD_FEATURE_CAPS_ALPHA_FILL</b> flag, the alpha fill mode must be set to <b>DXVAHD_ALPHA_FILL_MODE_OPAQUE</b>.

The default state value is <b>DXVAHD_ALPHA_FILL_MODE_OPAQUE</b>.

### -field StreamNumber

Zero-based index of the input stream to use for the alpha values. This member is used when the alpha fill mode is <b>DXVAHD_ALPHA_FILL_MODE_SOURCE_STREAM</b>; otherwise, the value is ignored. 

To get the maximum number of streams, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>MaxStreamStates</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_blt_state">DXVAHD_BLT_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>