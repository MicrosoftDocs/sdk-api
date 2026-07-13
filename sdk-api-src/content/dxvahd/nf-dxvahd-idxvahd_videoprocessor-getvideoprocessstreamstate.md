---
UID: NF:dxvahd.IDXVAHD_VideoProcessor.GetVideoProcessStreamState
title: IDXVAHD_VideoProcessor::GetVideoProcessStreamState (dxvahd.h)
description: Gets the value of a state parameter for an input stream on a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["GetVideoProcessStreamState","GetVideoProcessStreamState method [Media Foundation]","GetVideoProcessStreamState method [Media Foundation]","IDXVAHD_VideoProcessor interface","IDXVAHD_VideoProcessor interface [Media Foundation]","GetVideoProcessStreamState method","IDXVAHD_VideoProcessor.GetVideoProcessStreamState","IDXVAHD_VideoProcessor::GetVideoProcessStreamState","dxvahd/IDXVAHD_VideoProcessor::GetVideoProcessStreamState","mf.idxvahd_videoprocessor_getvideoprocessstreamstate"]
old-location: mf\idxvahd_videoprocessor_getvideoprocessstreamstate.htm
tech.root: mf
ms.assetid: 1ceeae95-d67d-4f11-b815-f4eef517e7ce
ms.date: 12/05/2018
ms.keywords: GetVideoProcessStreamState, GetVideoProcessStreamState method [Media Foundation], GetVideoProcessStreamState method [Media Foundation],IDXVAHD_VideoProcessor interface, IDXVAHD_VideoProcessor interface [Media Foundation],GetVideoProcessStreamState method, IDXVAHD_VideoProcessor.GetVideoProcessStreamState, IDXVAHD_VideoProcessor::GetVideoProcessStreamState, dxvahd/IDXVAHD_VideoProcessor::GetVideoProcessStreamState, mf.idxvahd_videoprocessor_getvideoprocessstreamstate
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
 - IDXVAHD_VideoProcessor::GetVideoProcessStreamState
 - dxvahd/IDXVAHD_VideoProcessor::GetVideoProcessStreamState
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
 - IDXVAHD_VideoProcessor.GetVideoProcessStreamState
---

# IDXVAHD_VideoProcessor::GetVideoProcessStreamState


## -description

Gets the value of a state parameter for an input stream on a  Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -parameters

### -param StreamNumber [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>MaxStreamStates</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure.

### -param State [in]

The state parameter to query, specified as a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a> enumeration.

### -param DataSize [in]

The size, in bytes, of the buffer pointed to by <i>pData</i>.

### -param pData [out]

A pointer to a buffer allocated by the caller. The method copies the state data into the buffer. The buffer must be large enough to hold the data structure that corresponds to the state parameter. For more information, see <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor">IDXVAHD_VideoProcessor</a>