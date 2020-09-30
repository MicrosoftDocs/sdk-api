---
UID: NF:d3d12video.ID3D12VideoDevice.CreateVideoProcessor
title: ID3D12VideoDevice::CreateVideoProcessor
description: Creates a video processor instance.
helpviewer_keywords: ["ID3D12VideoDevice::CreateVideoProcessor","CreateVideoProcessor","ID3D12VideoDevice.CreateVideoProcessor","ID3D12VideoDevice::CreateVideoProcessor","ID3D12VideoDevice.CreateVideoProcessor"]
tech.root: mf
ms.assetid: f19f0bfe-4b60-4f96-af85-fe7fec824875
ms.date: 05/28/2019
ms.keywords: ID3D12VideoDevice::CreateVideoProcessor, CreateVideoProcessor, ID3D12VideoDevice.CreateVideoProcessor, ID3D12VideoDevice::CreateVideoProcessor, ID3D12VideoDevice.CreateVideoProcessor
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
 - ID3D12VideoDevice::CreateVideoProcessor
 - d3d12video/ID3D12VideoDevice::CreateVideoProcessor
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDevice::CreateVideoProcessor
---

# ID3D12VideoDevice::CreateVideoProcessor


## -description

Creates a video processor instance.

## -parameters

### -param NodeMask

The node mask specifying the physical adapter on which the video processor will be used. For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node, i.e. the device's physical adapter, to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -param pOutputStreamDesc

A pointer to a D3D12\_VIDEO\_PROCESS\_OUTPUT\_STREAM\_DESC(ns-d3d12video-d3d12_video_process_output_stream_desc) structure describing the output stream.

### -param NumInputStreamDescs

The number of input streams provided in the *pInputStreamDescs* parameter.

### -param pInputStreamDescs

A pointer to a list of D3D12\_VIDEO\_PROCESS\_INPUT\_STREAM\_DESC(ns-d3d12video-d3d12_video_process_input_stream_desc) structures the input streams. The number of structures provided should match the value specified in the *NumInputStreamDescs* parameter.

### -param riid

The globally unique identifier (GUID) for the video processor interface.

### -param ppVideoProcessor

A pointer to a memory block that receives a pointer to the [ID3D12VideoProcessor](nn-d3d12video-id3d12videoprocessor.md) interface

## -returns

This method returns HRESULT.

## -remarks

To change the parameters set during creation, you must recreate the video processor object.

## -see-also

