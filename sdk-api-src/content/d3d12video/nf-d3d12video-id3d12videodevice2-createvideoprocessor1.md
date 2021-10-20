---
UID: NF:d3d12video.ID3D12VideoDevice2.CreateVideoProcessor1
title: ID3D12VideoDevice2::CreateVideoProcessor1
description: Creates a video processor instance with support for protected resources.
tech.root: mf
ms.date: 8/19/2019
ms.keywords: ID3D12VideoDevice2::CreateVideoProcessor1
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ID3D12VideoDevice2::CreateVideoProcessor1
 - d3d12video/ID3D12VideoDevice2::CreateVideoProcessor1
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoDevice2::CreateVideoProcessor1
---

## -description

Creates a video processor instance with support for protected resources.

## -parameters

### -param NodeMask

The node mask specifying the physical adapter on which the video processor will be used. For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node, i.e. the device's physical adapter, to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -param pOutputStreamDesc

A pointer to a D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC(ns-d3d12video-d3d12_video_process_output_stream_desc) structure describing the output stream.

### -param NumInputStreamDescs

The number of input streams provided in the *pInputStreamDescs* parameter.

### -param pInputStreamDescs

A pointer to a list of D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC(ns-d3d12video-d3d12_video_process_input_stream_desc) structures the input streams. The number of structures provided should match the value specified in the *NumInputStreamDescs* parameter.

### -param pProtectedResourceSession

A [ID3D12ProtectedResourceSession](../d3d12/nn-d3d12-id3d12protectedresourcesession.md) for managing access to protected resources.

### -param riid

The globally unique identifier (GUID) for the video processor interface.

### -param ppVideoProcessor

A pointer to a memory block that receives a pointer to the [ID3D12VideoProcessor1](nn-d3d12video-id3d12videoprocessor1.md) interface

## -returns

This method returns HRESULT.

## -remarks

To change the parameters set during creation, you must recreate the video processor object.

## -see-also
