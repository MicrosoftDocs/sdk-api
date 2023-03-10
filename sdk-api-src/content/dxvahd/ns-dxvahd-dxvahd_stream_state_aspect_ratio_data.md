---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA
title: DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA (dxvahd.h)
description: Specifies the pixel aspect ratio (PAR) for the source and destination rectangles.
helpviewer_keywords: ["DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA","DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA structure [Media Foundation]","PDXVAHD_STREAM_STATE_ASPECT_RATIO_DATA","PDXVAHD_STREAM_STATE_ASPECT_RATIO_DATA structure pointer [Media Foundation]","dxvahd/DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA","dxvahd/PDXVAHD_STREAM_STATE_ASPECT_RATIO_DATA","mf.dxvahd_stream_state_aspect_ratio_data"]
old-location: mf\dxvahd_stream_state_aspect_ratio_data.htm
tech.root: mf
ms.assetid: dd7ab16e-2dc6-462e-b55d-b93a14c362cf
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA, DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA structure [Media Foundation], PDXVAHD_STREAM_STATE_ASPECT_RATIO_DATA, PDXVAHD_STREAM_STATE_ASPECT_RATIO_DATA structure pointer [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA, dxvahd/PDXVAHD_STREAM_STATE_ASPECT_RATIO_DATA, mf.dxvahd_stream_state_aspect_ratio_data
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
req.typenames: DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA
 - DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA
 - dxvahd/DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA
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
 - DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA
---

# DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA structure


## -description

Specifies the pixel aspect ratio (PAR) for the source and destination rectangles.

## -struct-fields

### -field Enable

<b>If TRUE</b>, the <b>SourceAspectRatio</b> and <b>DestinationAspectRatio</b> members contain valid values<b></b>. Otherwise, the pixel aspect ratios are unspecified.

### -field SourceAspectRatio

A <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_rational">DXVAHD_RATIONAL</a> structure that contains the source PAR. The default state value is 1:1 (square pixels).

### -field DestinationAspectRatio

A <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_rational">DXVAHD_RATIONAL</a> structure that contains the destination PAR. The default state value is 1:1 (square pixels).

## -remarks

Pixel aspect ratios of the form 0/<i>n</i> and <i>n</i>/0 are not valid.

If the <b>Enable</b> member is <b>FALSE</b>, the device ignores the values of <b>SourceAspectRatio</b> and <b>DestinationAspectRatio</b>.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/picture-aspect-ratio">Picture Aspect Ratio</a>