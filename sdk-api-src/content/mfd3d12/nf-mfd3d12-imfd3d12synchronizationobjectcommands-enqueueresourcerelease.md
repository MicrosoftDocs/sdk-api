---
UID: NF:mfd3d12.IMFD3D12SynchronizationObjectCommands.EnqueueResourceRelease
tech.root: mf
title: IMFD3D12SynchronizationObjectCommands::EnqueueResourceRelease
ms.date: 07/27/2021
targetos: Windows
description: Queues a fence into the specified command queue that will signal to the synchronization object when GPU is finished processing the consumer commands.
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
 - IMFD3D12SynchronizationObjectCommands::EnqueueResourceRelease
f1_keywords:
 - IMFD3D12SynchronizationObjectCommands::EnqueueResourceRelease
 - mfd3d12/IMFD3D12SynchronizationObjectCommands::EnqueueResourceRelease
dev_langs:
 - c++
---

## -description

Queues a fence into the specified command queue that will signal to the synchronization object when GPU is finished processing the consumer commands.  This method signals when the resource is no longer in use and has been released by the consumer.

## -parameters

### -param pConsumerCommandQueue

A pointer to an [ID3D12CommandQueue](../d3d12/nn-d3d12-id3d12commandqueue.md) representing the consumer command queue onto which the fence should be queued.

## -returns

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| MF_E_OPERATION_UNSUPPORTED_AT_D3D_FEATURE_LEVEL | The attempted call or command is not supported with the DirectX version used by the component. |
| o	MF_E_UNSUPPORTED_MEDIATYPE_AT_D3D_FEATURE_LEVEL | The specified media type is not supported with the DirectX version used by the component. |

## -remarks

## -see-also

