---
UID: NF:mfd3d12.MFCreateD3D12SynchronizationObject
tech.root: mf
title: MFCreateD3D12SynchronizationObject
ms.date: 07/27/2021
targetos: Windows
description: Instantiates an a Media Foundation D3D12 synchronization primitive used to synchronize access to a D3D12 resource stored in an Media Foundation object.
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
req.lib: Mfplat.lib
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
 - HeaderDef
api_location:
 - mfd3d12.h
api_name:
 - MFCreateD3D12SynchronizationObject
f1_keywords:
 - MFCreateD3D12SynchronizationObject
 - mfd3d12/MFCreateD3D12SynchronizationObject
dev_langs:
 - c++
---

## -description

Instantiates an a Media Foundation D3D12 synchronization primitive used to synchronize access to a D3D12 resource stored in an Media Foundation object.


## -parameters

### -param pDevice

The [ID3D12Device](../d3d12/nn-d3d12-id3d12device.md) associated with the resource and primitive being created.

### -param riid

The GUID identifying the interface of the synchronization object that will be created.

### -param ppvSyncObject

Receives a **void\*\*** pointing to the created synchronization object.

## -returns

An HRESULT including but not limited to the following values:

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| MF_E_OPERATION_UNSUPPORTED_AT_D3D_FEATURE_LEVEL | The attempted call or command is not supported with the DirectX version used by the component. |
| o	MF_E_UNSUPPORTED_MEDIATYPE_AT_D3D_FEATURE_LEVEL | The specified media type is not supported with the DirectX version used by the component. |

## -remarks

## -see-also

