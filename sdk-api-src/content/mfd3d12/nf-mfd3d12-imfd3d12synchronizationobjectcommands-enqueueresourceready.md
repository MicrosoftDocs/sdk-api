---
UID: NF:mfd3d12.IMFD3D12SynchronizationObjectCommands.EnqueueResourceReady
tech.root: mf
title: IMFD3D12SynchronizationObjectCommands::EnqueueResourceReady
ms.date: 07/27/2021
targetos: Windows
description: Queues a fence on the specified producer command queue that will signal to a downstream consumer when the associated D3D12 resource is ready to be used.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfd3d12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfd3d12.h
api_name:
 - IMFD3D12SynchronizationObjectCommands::EnqueueResourceReady
f1_keywords:
 - IMFD3D12SynchronizationObjectCommands::EnqueueResourceReady
 - mfd3d12/IMFD3D12SynchronizationObjectCommands::EnqueueResourceReady
dev_langs:
 - c++
---

## -description

Queues a fence on the specified producer command queue that will signal to a downstream consumer when the associated D3D12 resource is ready to be used. This method also signals that the resource is no longer in use and has been released by the producer.


## -parameters

### -param pProducerCommandQueue

A pointer to an [ID3D12CommandQueue](../d3d12/nn-d3d12-id3d12commandqueue.md) representing the producer command queue into which the fence should be inserted.

## -returns

An HRESULT including but not limited to the following values:

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| MF_E_OPERATION_UNSUPPORTED_AT_D3D_FEATURE_LEVEL | The attempted call or command is not supported with the DirectX version used by the component. |
| o	MF_E_UNSUPPORTED_MEDIATYPE_AT_D3D_FEATURE_LEVEL | The specified media type is not supported with the DirectX version used by the component. |

## -remarks

This method will be used by a producer to signal to a down-stream consumer when all the GPU commands that the producer scheduled for the resource have been processed. The signal indicates that the resource is ready for consumption by the consumer.

## -see-also

