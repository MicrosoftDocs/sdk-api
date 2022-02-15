---
UID: NE:dxvahd._DXVAHD_FRAME_FORMAT
title: DXVAHD_FRAME_FORMAT (dxvahd.h)
description: Describes how a video stream is interlaced.
helpviewer_keywords: ["DXVAHD_FRAME_FORMAT","DXVAHD_FRAME_FORMAT enumeration [Media Foundation]","DXVAHD_FRAME_FORMAT_INTERLACED_BOTTOM_FIELD_FIRST","DXVAHD_FRAME_FORMAT_INTERLACED_TOP_FIELD_FIRST","DXVAHD_FRAME_FORMAT_PROGRESSIVE","dxvahd/DXVAHD_FRAME_FORMAT","dxvahd/DXVAHD_FRAME_FORMAT_INTERLACED_BOTTOM_FIELD_FIRST","dxvahd/DXVAHD_FRAME_FORMAT_INTERLACED_TOP_FIELD_FIRST","dxvahd/DXVAHD_FRAME_FORMAT_PROGRESSIVE","mf.dxvahd_frame_format"]
old-location: mf\dxvahd_frame_format.htm
tech.root: mf
ms.assetid: fc720dd3-e9c1-4b92-ac09-8e53cff44bec
ms.date: 12/05/2018
ms.keywords: DXVAHD_FRAME_FORMAT, DXVAHD_FRAME_FORMAT enumeration [Media Foundation], DXVAHD_FRAME_FORMAT_INTERLACED_BOTTOM_FIELD_FIRST, DXVAHD_FRAME_FORMAT_INTERLACED_TOP_FIELD_FIRST, DXVAHD_FRAME_FORMAT_PROGRESSIVE, dxvahd/DXVAHD_FRAME_FORMAT, dxvahd/DXVAHD_FRAME_FORMAT_INTERLACED_BOTTOM_FIELD_FIRST, dxvahd/DXVAHD_FRAME_FORMAT_INTERLACED_TOP_FIELD_FIRST, dxvahd/DXVAHD_FRAME_FORMAT_PROGRESSIVE, mf.dxvahd_frame_format
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
req.typenames: DXVAHD_FRAME_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_FRAME_FORMAT
 - dxvahd/_DXVAHD_FRAME_FORMAT
 - DXVAHD_FRAME_FORMAT
 - dxvahd/DXVAHD_FRAME_FORMAT
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
 - DXVAHD_FRAME_FORMAT
---

# DXVAHD_FRAME_FORMAT enumeration


## -description

Describes how a video stream is interlaced.

## -enum-fields

### -field DXVAHD_FRAME_FORMAT_PROGRESSIVE:0

Frames are progressive.

### -field DXVAHD_FRAME_FORMAT_INTERLACED_TOP_FIELD_FIRST:1

Frames are interlaced. The top field of each frame is displayed first.

### -field DXVAHD_FRAME_FORMAT_INTERLACED_BOTTOM_FIELD_FIRST:2

Frame are interlaced. The bottom field of each frame is displayed first.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc">DXVAHD_CONTENT_DESC</a>



<a href="/windows/win32/api/dxvahd/ns-dxvahd-dxvahd_stream_state_frame_format_data">DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
