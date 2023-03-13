---
UID: NF:d3d12.ID3D12Device7.AddToStateObject
title: ID3D12Device7::AddToStateObject
description: Incrementally add to an existing state object. This incurs lower CPU overhead than creating a state object from scratch that is a superset of an existing one.
helpviewer_keywords: ["ID3D12Device7 interface","AddToStateObject method","ID3D12Device7.AddToStateObject","ID3D12Device7::AddToStateObject","AddToStateObject","AddToStateObject method","AddToStateObject method","ID3D12Device7 interface","direct3d12.id3d12device7_addtostateobject","d3d12/ID3D12Device7::AddToStateObject"]
tech.root: direct3d12
ms.date: 09/15/2020
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
 - ID3D12Device7::AddToStateObject
f1_keywords:
 - d3d12/ID3D12Device7::AddToStateObject
dev_langs:
 - c++
---

## -description

Incrementally add to an existing state object. This incurs lower CPU overhead than creating a state object from scratch that is a superset of an existing one (for example, adding a few more shaders).

## -parameters

### -param pAddition

Type: \_In\_ **const [D3D12_STATE_OBJECT_DESC](./ns-d3d12-d3d12_state_object_desc.md)\***

Description of state object contents to add to existing state object. To help generate this see the **CD3D12_STATE_OBJECT_DESC** helper in class in `d3dx12.h`.

### -param pStateObjectToGrowFrom

Type: \_In\_ **[ID3D12StateObject](./nn-d3d12-id3d12stateobject.md)\***

Existing state object, which can be in use (for example, active raytracing) during this operation.

The existing state object must not be of type **Collection**.

### -param riid

Type: \_In\_ **REFIID**

Must be the IID of the [ID3D12StateObject](./nn-d3d12-id3d12stateobject.md) interface.

### -param ppNewStateObject

Type: \_COM\_Outptr\_ **void\*\***

Returned state object.

Behavior is undefined if shader identifiers are retrieved for new shaders from this call and they are accessed via shader tables by any already existing or in-flight command list that references some older state object. Use of the new shaders added to the state object can occur only from commands (such as **DispatchRays** or **ExecuteIndirect** calls) recorded in a command list after the call to **AddToStateObject**.

## -returns

**S_OK** for success. **E_INVALIDARG**, **E_OUTOFMEMORY** on failure. The debug layer provides detailed status information.

## -remarks

For more info, see [AddToStateObject](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#addtostateobject).

## -see-also
