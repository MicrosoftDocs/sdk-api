---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_D3DFORMAT_DATA
title: DXVAHD_STREAM_STATE_D3DFORMAT_DATA (dxvahd.h)
description: Specifies the format for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_STREAM_STATE_D3DFORMAT_DATA","DXVAHD_STREAM_STATE_D3DFORMAT_DATA structure [Media Foundation]","dxvahd/DXVAHD_STREAM_STATE_D3DFORMAT_DATA","mf.dxvahd_stream_state_d3dformat_data"]
old-location: mf\dxvahd_stream_state_d3dformat_data.htm
tech.root: mf
ms.assetid: a1ba825b-0574-4657-8a10-447a3caf8149
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_D3DFORMAT_DATA, DXVAHD_STREAM_STATE_D3DFORMAT_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_D3DFORMAT_DATA, mf.dxvahd_stream_state_d3dformat_data
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
req.typenames: DXVAHD_STREAM_STATE_D3DFORMAT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_D3DFORMAT_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_D3DFORMAT_DATA
 - DXVAHD_STREAM_STATE_D3DFORMAT_DATA
 - dxvahd/DXVAHD_STREAM_STATE_D3DFORMAT_DATA
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
 - DXVAHD_STREAM_STATE_D3DFORMAT_DATA
---

# DXVAHD_STREAM_STATE_D3DFORMAT_DATA structure


## -description

Specifies the format for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

## -struct-fields

### -field Format

The surface format, specified as a <b>D3DFORMAT</b> value. You can also use a FOURCC code to specify a format that is not defined in the <b>D3DFORMAT</b> enumeration. For more information, see <a href="/windows/desktop/medfound/video-fourccs">Video FOURCCs</a>.

The default state value is <b>D3DFMT_UNKNOWN</b>.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>