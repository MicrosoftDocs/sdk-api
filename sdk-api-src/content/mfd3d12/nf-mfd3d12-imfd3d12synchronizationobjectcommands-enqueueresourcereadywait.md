---
UID: NF:mfd3d12.IMFD3D12SynchronizationObjectCommands.EnqueueResourceReadyWait
tech.root: mf
title: IMFD3D12SynchronizationObjectCommands::EnqueueResourceReadyWait
ms.date: 07/27/2021
targetos: Windows
description: Queues a wait command on the specified consumer command queue, starting a wait for the resource ready signal from the producer command queue. 
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
 - IMFD3D12SynchronizationObjectCommands::EnqueueResourceReadyWait
f1_keywords:
 - IMFD3D12SynchronizationObjectCommands::EnqueueResourceReadyWait
 - mfd3d12/IMFD3D12SynchronizationObjectCommands::EnqueueResourceReadyWait
dev_langs:
 - c++
---

## -description

Queues a wait command on the specified consumer command queue, starting a wait for the
resource ready signal from the producer command queue.  


## -parameters

### -param pConsumerCommandQueue

A pointer to an [ID3D12CommandQueue](../d3d12/nn-d3d12-id3d12commandqueue.md) representing the consumer command queue into which the wait should be queued.

## -returns

An HRESULT including but not limited to the following values:

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| MF_E_OPERATION_UNSUPPORTED_AT_D3D_FEATURE_LEVEL | The attempted call or command is not supported with the DirectX version used by the component. |
| o	MF_E_UNSUPPORTED_MEDIATYPE_AT_D3D_FEATURE_LEVEL | The specified media type is not supported with the DirectX version used by the component. |

## -remarks

This function allows the consumer to immediately start scheduling commands for its GPU engine.  The wait will ensure that the commands scheduled after the wait are not executed until the corresponding ready signal is fired by the producer GPU engine.

## -see-also

