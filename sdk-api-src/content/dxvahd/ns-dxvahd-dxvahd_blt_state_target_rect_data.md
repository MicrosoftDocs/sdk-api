---
UID: NS:dxvahd._DXVAHD_BLT_STATE_TARGET_RECT_DATA
title: DXVAHD_BLT_STATE_TARGET_RECT_DATA (dxvahd.h)
description: Specifies the target rectangle for blitting, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_BLT_STATE_TARGET_RECT_DATA","DXVAHD_BLT_STATE_TARGET_RECT_DATA structure [Media Foundation]","FALSE","TRUE","dxvahd/DXVAHD_BLT_STATE_TARGET_RECT_DATA","mf.dxvahd_blt_state_target_rect_data"]
old-location: mf\dxvahd_blt_state_target_rect_data.htm
tech.root: mf
ms.assetid: 2a810071-b5f7-4216-8108-83dce5c12836
ms.date: 12/05/2018
ms.keywords: DXVAHD_BLT_STATE_TARGET_RECT_DATA, DXVAHD_BLT_STATE_TARGET_RECT_DATA structure [Media Foundation], FALSE, TRUE, dxvahd/DXVAHD_BLT_STATE_TARGET_RECT_DATA, mf.dxvahd_blt_state_target_rect_data
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
req.typenames: DXVAHD_BLT_STATE_TARGET_RECT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_BLT_STATE_TARGET_RECT_DATA
 - dxvahd/_DXVAHD_BLT_STATE_TARGET_RECT_DATA
 - DXVAHD_BLT_STATE_TARGET_RECT_DATA
 - dxvahd/DXVAHD_BLT_STATE_TARGET_RECT_DATA
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
 - DXVAHD_BLT_STATE_TARGET_RECT_DATA
---

# DXVAHD_BLT_STATE_TARGET_RECT_DATA structure


## -description

Specifies the target rectangle for blitting, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

## -struct-fields

### -field Enable

Specifies whether to use the target rectangle. The default state value is <b>FALSE</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Use the target rectangle specified by the <b>TargetRect</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Use the entire destination surface as the target rectangle. Ignore the <b>TargetRect</b> member.

</td>
</tr>
</table>

### -field TargetRect

Specifies the <i>target rectangle</i>. The target rectangle is the area within the destination surface where the output will be drawn. The target rectangle is given in pixel coordinates, relative to the destination surface. The default state value is an empty rectangle, (0, 0, 0, 0).

If the <b>Enable</b> member is <b>FALSE</b>, the <b>TargetRect</b> member is ignored.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_blt_state">DXVAHD_BLT_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>