---
UID: NC:dxvahd.PDXVAHDSW_SetVideoProcessStreamState
title: PDXVAHDSW_SetVideoProcessStreamState (dxvahd.h)
description: Sets a state parameter for an input stream on a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
helpviewer_keywords: ["PDXVAHDSW_SetVideoProcessStreamState","PDXVAHDSW_SetVideoProcessStreamState callback","PDXVAHDSW_SetVideoProcessStreamState callback function [Media Foundation]","dxvahd/PDXVAHDSW_SetVideoProcessStreamState","mf.pdxvahdsw_setvideoprocessstreamstate"]
old-location: mf\pdxvahdsw_setvideoprocessstreamstate.htm
tech.root: mf
ms.assetid: 1fbecdbd-9f04-4d1e-82a6-4c6ce522cdaf
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_SetVideoProcessStreamState, PDXVAHDSW_SetVideoProcessStreamState callback, PDXVAHDSW_SetVideoProcessStreamState callback function [Media Foundation], dxvahd/PDXVAHDSW_SetVideoProcessStreamState, mf.pdxvahdsw_setvideoprocessstreamstate
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDXVAHDSW_SetVideoProcessStreamState
 - dxvahd/PDXVAHDSW_SetVideoProcessStreamState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxvahd.h
api_name:
 - PDXVAHDSW_SetVideoProcessStreamState
---

# PDXVAHDSW_SetVideoProcessStreamState callback function


## -description

Sets a state parameter for an input stream on a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

## -parameters

### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.

### -param StreamNumber [in]

The zero-based index of the input stream.

### -param State [in]

The state parameter to set, specified as a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a> enumeration.

### -param DataSize [in]

The size of the buffer pointed to by <i>pData</i>, in bytes.

### -param pData [in]

A pointer to a buffer that contains the state data.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
