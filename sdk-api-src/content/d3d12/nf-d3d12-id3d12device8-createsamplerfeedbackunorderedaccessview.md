---
UID: NF:d3d12.ID3D12Device8.CreateSamplerFeedbackUnorderedAccessView
title: ID3D12Device8::CreateSamplerFeedbackUnorderedAccessView
description: For purposes of sampler feedback, creates a descriptor suitable for binding.
helpviewer_keywords: ["ID3D12Device8 interface","CreateSamplerFeedbackUnorderedAccessView method","ID3D12Device8.CreateSamplerFeedbackUnorderedAccessView","ID3D12Device8::CreateSamplerFeedbackUnorderedAccessView","CreateSamplerFeedbackUnorderedAccessView","CreateSamplerFeedbackUnorderedAccessView method","CreateSamplerFeedbackUnorderedAccessView method","ID3D12Device8 interface","direct3d12.id3d12device7_createsamplerfeedbackunorderedaccessview","d3d12/ID3D12Device8::CreateSamplerFeedbackUnorderedAccessView"]
tech.root: direct3d12
ms.date: 09/16/2020
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: d3d12.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.lib
 - d3d12.dll
api_name:
 - ID3D12Device8::CreateSamplerFeedbackUnorderedAccessView
f1_keywords:
 - d3d12/ID3D12Device8::CreateSamplerFeedbackUnorderedAccessView
dev_langs:
 - c++
---

## -description

For purposes of sampler feedback, creates a descriptor suitable for binding.

## -parameters

### -param pTargetedResource

Type: \_In\_opt\_ **[ID3D12Resource](./nn-d3d12-id3d12heap.md)\***

The targeted resource, such as a texture, to create a descriptor for.

### -param pFeedbackResource

Type: \_In\_opt\_ **[ID3D12Resource](./nn-d3d12-id3d12heap.md)\***

The feedback resource, such as a texture, to create a descriptor for.

### -param DestDescriptor

Type: \_In\_ **[D3D12_CPU_DESCRIPTOR_HANDLE](./ns-d3d12-d3d12_cpu_descriptor_handle.md)**

The CPU descriptor handle.

## -see-also

* [Sampler feedback specification](https://microsoft.github.io/DirectX-Specs/d3d/SamplerFeedback.html)
