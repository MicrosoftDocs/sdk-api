---
UID: NS:d3d12.D3D12_STATE_SUBOBJECT
title: D3D12_STATE_SUBOBJECT (d3d12.h)
description: Represents a subobject within a state object description. Use with [D3D12_STATE_OBJECT_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc).
helpviewer_keywords: ["D3D12_STATE_SUBOBJECT","D3D12_STATE_SUBOBJECT structure","PD3D12_STATE_SUBOBJECT","PD3D12_STATE_SUBOBJECT structure pointer","d3d12/D3D12_STATE_SUBOBJECT","d3d12/PD3D12_STATE_SUBOBJECT","direct3d12.d3d12_state_subobject"]
old-location: direct3d12\d3d12_state_subobject.htm
tech.root: direct3d12
ms.assetid: D721F0F2-B061-4BDC-83F7-7B08DDC39F34
ms.date: 12/05/2018
ms.keywords: D3D12_STATE_SUBOBJECT, D3D12_STATE_SUBOBJECT structure, PD3D12_STATE_SUBOBJECT, PD3D12_STATE_SUBOBJECT structure pointer, d3d12/D3D12_STATE_SUBOBJECT, d3d12/PD3D12_STATE_SUBOBJECT, direct3d12.d3d12_state_subobject
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_STATE_SUBOBJECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_STATE_SUBOBJECT
 - d3d12/D3D12_STATE_SUBOBJECT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_STATE_SUBOBJECT
---

## -description

Represents a subobject within a state object description. Use with [D3D12_STATE_OBJECT_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc).

## -struct-fields

### -field Type

A [D3D12_STATE_SUBOBJECT_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) specifying the type of the state subobject.

### -field pDesc

Pointer to state object description of the type specified in the *Type* parameter.
