---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA
title: DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA (dxvahd.h)
description: Specifies the destination rectangle for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA","DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA structure [Media Foundation]","FALSE","TRUE","dxvahd/DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA","mf.dxvahd_stream_state_destination_rect_data"]
old-location: mf\dxvahd_stream_state_destination_rect_data.htm
tech.root: mf
ms.assetid: f850531b-eee0-4943-8c41-050ec78eab63
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA, DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA structure [Media Foundation], FALSE, TRUE, dxvahd/DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA, mf.dxvahd_stream_state_destination_rect_data
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
req.typenames: DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA
 - DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA
 - dxvahd/DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA
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
 - DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA
---

# DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA structure


## -description

Specifies the destination rectangle for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

## -struct-fields

### -field Enable

Specifies whether to use the destination rectangle, or use the entire output surface. The default state value is <b>FALSE</b>.

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
Use the destination rectangle given in the <b>DestinationRect</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Use the entire output surface as the destination rectangle.

</td>
</tr>
</table>

### -field DestinationRect

The <i>destination rectangle</i>, which defines the portion of the output surface where the source rectangle is blitted. The destination rectangle is given in pixel coordinates, relative to the output surface. The default value is an empty rectangle, (0, 0, 0, 0).

If the <b>Enable</b> member is <b>FALSE</b>, the <b>DestinationRect</b> member is ignored.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>