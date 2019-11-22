---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessStreamStatePrivate
title: PDXVAHDSW_GetVideoProcessStreamStatePrivate (dxvahd.h)

description: Gets a private stream state from a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\pdxvahdsw_getvideoprocessstreamstateprivate.htm
tech.root: medfound
ms.assetid: db751314-8c3c-4969-87c4-0b2b2201ce20

ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_GetVideoProcessStreamStatePrivate, PDXVAHDSW_GetVideoProcessStreamStatePrivate callback, PDXVAHDSW_GetVideoProcessStreamStatePrivate callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessStreamStatePrivate, mf.pdxvahdsw_getvideoprocessstreamstateprivate
ms.topic: callback
f1_keywords:
- dxvahd/PDXVAHDSW_GetVideoProcessStreamStatePrivate
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- dxvahd.h
api_name:
- PDXVAHDSW_GetVideoProcessStreamStatePrivate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDXVAHDSW_GetVideoProcessStreamStatePrivate callback function


## -description


Gets a private stream state from a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -parameters




### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.


### -param StreamNumber [in]

The zero-based index of the input stream.


### -param *pData [in, out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_private_data">DXVAHD_STREAM_STATE_PRIVATE_DATA</a> structure. On input, the <b>Guid</b> member specifies the private state to query. On output, the structure contains the state information.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-getvideoprocessstreamstate">IDXVAHD_VideoProcessor::GetVideoProcessStreamState</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

