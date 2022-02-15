---
UID: NF:d3d12video.ID3D12VideoProcessor.GetNumInputStreamDescs
title: ID3D12VideoProcessor::GetNumInputStreamDescs
description: Gets the number of input stream descriptions provided when the video processor was created with a call to ID3D12VideoDevice::CreateVideoProcessor.
helpviewer_keywords: ["ID3D12VideoProcessor::GetNumInputStreamDescs","GetNumInputStreamDescs","ID3D12VideoProcessor.GetNumInputStreamDescs","ID3D12VideoProcessor::GetNumInputStreamDescs","ID3D12VideoProcessor.GetNumInputStreamDescs"]
tech.root: mf
ms.assetid: 3e749d39-ade5-4d52-9d91-4a98ca5650b6
ms.date: 05/28/2019
ms.keywords: ID3D12VideoProcessor::GetNumInputStreamDescs, GetNumInputStreamDescs, ID3D12VideoProcessor.GetNumInputStreamDescs, ID3D12VideoProcessor::GetNumInputStreamDescs, ID3D12VideoProcessor.GetNumInputStreamDescs
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
 - ID3D12VideoProcessor::GetNumInputStreamDescs
 - d3d12video/ID3D12VideoProcessor::GetNumInputStreamDescs
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessor::GetNumInputStreamDescs
---

# ID3D12VideoProcessor::GetNumInputStreamDescs


## -description

Gets the number of input stream descriptions provided when the video processor was created with a call to [ID3D12VideoDevice::CreateVideoProcessor](nf-d3d12video-id3d12videodevice-createvideoprocessor.md).



## -returns

This method returns UINT. Use this value to determine the correct size of the array you pass in the *pInputStreamDescs* parameter to [ID3D12VideoProcessor::GetInputStreamDescs](nf-d3d12video-id3d12videoprocessor-getinputstreamdescs.md).

## -remarks

## -see-also

