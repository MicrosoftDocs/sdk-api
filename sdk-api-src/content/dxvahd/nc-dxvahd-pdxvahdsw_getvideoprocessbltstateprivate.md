---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessBltStatePrivate
title: PDXVAHDSW_GetVideoProcessBltStatePrivate (dxvahd.h)
description: Gets a private blit state from a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
helpviewer_keywords: ["PDXVAHDSW_GetVideoProcessBltStatePrivate","PDXVAHDSW_GetVideoProcessBltStatePrivate callback","PDXVAHDSW_GetVideoProcessBltStatePrivate callback function [Media Foundation]","dxvahd/PDXVAHDSW_GetVideoProcessBltStatePrivate","mf.pdxvahdsw_getvideoprocessbltstateprivate"]
old-location: mf\pdxvahdsw_getvideoprocessbltstateprivate.htm
tech.root: mf
ms.assetid: 32154457-5270-4e60-a16c-bca72c6a9673
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_GetVideoProcessBltStatePrivate, PDXVAHDSW_GetVideoProcessBltStatePrivate callback, PDXVAHDSW_GetVideoProcessBltStatePrivate callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessBltStatePrivate, mf.pdxvahdsw_getvideoprocessbltstateprivate
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
 - PDXVAHDSW_GetVideoProcessBltStatePrivate
 - dxvahd/PDXVAHDSW_GetVideoProcessBltStatePrivate
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
 - PDXVAHDSW_GetVideoProcessBltStatePrivate
---

# PDXVAHDSW_GetVideoProcessBltStatePrivate callback function


## -description

Gets a private blit state from a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

## -parameters

### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.

### -param pData [in, out]

A pointer to a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_blt_state_private_data">DXVAHD_BLT_STATE_PRIVATE_DATA</a> structure. On input, the <b>Guid</b> member specifies the private state to query. On output, the structure contains the state information.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-getvideoprocessbltstate">IDXVAHD_VideoProcessor::GetVideoProcessBltState</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
