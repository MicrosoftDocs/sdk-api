---
UID: NF:d3d12video.ID3D12VideoProcessor.GetInputStreamDescs
title: ID3D12VideoProcessor::GetInputStreamDescs
description: Gets the input stream descriptions provided when the video processor was created with a call to ID3D12VideoDevice::CreateVideoProcessor.
helpviewer_keywords: ["ID3D12VideoProcessor::GetInputStreamDescs","GetInputStreamDescs","ID3D12VideoProcessor.GetInputStreamDescs","ID3D12VideoProcessor::GetInputStreamDescs","ID3D12VideoProcessor.GetInputStreamDescs"]
tech.root: mf
ms.assetid: 1973387b-966f-4a85-8a28-74a324d80697
ms.date: 05/28/2019
ms.keywords: ID3D12VideoProcessor::GetInputStreamDescs, GetInputStreamDescs, ID3D12VideoProcessor.GetInputStreamDescs, ID3D12VideoProcessor::GetInputStreamDescs, ID3D12VideoProcessor.GetInputStreamDescs
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: d3d12.dll
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
f1_keywords:
 - ID3D12VideoProcessor::GetInputStreamDescs
 - d3d12video/ID3D12VideoProcessor::GetInputStreamDescs
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessor::GetInputStreamDescs
---

# ID3D12VideoProcessor::GetInputStreamDescs


## -description

Gets the input stream descriptions provided when the video processor was created with a call to [ID3D12VideoDevice::CreateVideoProcessor](nf-d3d12video-id3d12videodevice-createvideoprocessor.md).

## -parameters

### -param NumInputStreamDescs

The size of the array pointed to by *pInputStreamDescs*. Get the number of input stream descriptions associated with the video processor by calling [ID3DVideoProcessor::GetNumInputStreamDescs](nf-d3d12video-id3d12videoprocessor-getnuminputstreamdescs.md).

### -param pInputStreamDescs

An array of [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC](ns-d3d12video-d3d12_video_process_input_stream_desc.md) structures that is populated with the input stream descriptions associated with the video processor.

## -returns

This method returns HRESULT.

## -remarks

## -see-also

