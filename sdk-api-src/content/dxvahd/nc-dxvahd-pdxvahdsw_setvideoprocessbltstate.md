---
UID: NC:dxvahd.PDXVAHDSW_SetVideoProcessBltState
title: PDXVAHDSW_SetVideoProcessBltState (dxvahd.h)
description: Sets a state parameter for blit operations by a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
helpviewer_keywords: ["PDXVAHDSW_SetVideoProcessBltState","PDXVAHDSW_SetVideoProcessBltState callback","PDXVAHDSW_SetVideoProcessBltState callback function [Media Foundation]","dxvahd/PDXVAHDSW_SetVideoProcessBltState","mf.pdxvahdsw_setvideoprocessbltstate"]
old-location: mf\pdxvahdsw_setvideoprocessbltstate.htm
tech.root: mf
ms.assetid: 604af2f8-42e8-465c-a49f-8c6c9bcc84dd
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_SetVideoProcessBltState, PDXVAHDSW_SetVideoProcessBltState callback, PDXVAHDSW_SetVideoProcessBltState callback function [Media Foundation], dxvahd/PDXVAHDSW_SetVideoProcessBltState, mf.pdxvahdsw_setvideoprocessbltstate
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
 - PDXVAHDSW_SetVideoProcessBltState
 - dxvahd/PDXVAHDSW_SetVideoProcessBltState
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
 - PDXVAHDSW_SetVideoProcessBltState
---

# PDXVAHDSW_SetVideoProcessBltState callback function


## -description

Sets a state parameter for blit operations by a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

## -parameters

### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.

### -param State [in]

The state parameter to set, specified as a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_blt_state">DXVAHD_BLT_STATE</a> enumeration.

### -param DataSize [in]

The size of the buffer pointed to by <i>pData</i>, in bytes.

### -param pData [in]

A pointer to a buffer that contains the state data.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
