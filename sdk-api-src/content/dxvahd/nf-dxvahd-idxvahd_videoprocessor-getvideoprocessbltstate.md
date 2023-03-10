---
UID: NF:dxvahd.IDXVAHD_VideoProcessor.GetVideoProcessBltState
title: IDXVAHD_VideoProcessor::GetVideoProcessBltState (dxvahd.h)
description: Gets the value of a state parameter for blit operations performed by a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["GetVideoProcessBltState","GetVideoProcessBltState method [Media Foundation]","GetVideoProcessBltState method [Media Foundation]","IDXVAHD_VideoProcessor interface","IDXVAHD_VideoProcessor interface [Media Foundation]","GetVideoProcessBltState method","IDXVAHD_VideoProcessor.GetVideoProcessBltState","IDXVAHD_VideoProcessor::GetVideoProcessBltState","dxvahd/IDXVAHD_VideoProcessor::GetVideoProcessBltState","mf.idxvahd_videoprocessor_getvideoprocessbltstate"]
old-location: mf\idxvahd_videoprocessor_getvideoprocessbltstate.htm
tech.root: mf
ms.assetid: 5fdb0d39-7a64-41fd-8f70-4085ddbc7ebc
ms.date: 12/05/2018
ms.keywords: GetVideoProcessBltState, GetVideoProcessBltState method [Media Foundation], GetVideoProcessBltState method [Media Foundation],IDXVAHD_VideoProcessor interface, IDXVAHD_VideoProcessor interface [Media Foundation],GetVideoProcessBltState method, IDXVAHD_VideoProcessor.GetVideoProcessBltState, IDXVAHD_VideoProcessor::GetVideoProcessBltState, dxvahd/IDXVAHD_VideoProcessor::GetVideoProcessBltState, mf.idxvahd_videoprocessor_getvideoprocessbltstate
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
 - IDXVAHD_VideoProcessor::GetVideoProcessBltState
 - dxvahd/IDXVAHD_VideoProcessor::GetVideoProcessBltState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_VideoProcessor.GetVideoProcessBltState
---

# IDXVAHD_VideoProcessor::GetVideoProcessBltState


## -description

Gets the value of a state parameter for blit operations performed by a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -parameters

### -param State [in]

The state parameter to query, specified as a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_blt_state">DXVAHD_BLT_STATE</a> enumeration.

### -param DataSize [in]

The size, in bytes, of the buffer pointed to by <i>pData</i>.

### -param pData [out]

A pointer to a buffer allocated by the caller. The method copies the state data into the buffer. The buffer must be large enough to hold the data structure that corresponds to the state parameter. For more information, see <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_blt_state">DXVAHD_BLT_STATE</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor">IDXVAHD_VideoProcessor</a>