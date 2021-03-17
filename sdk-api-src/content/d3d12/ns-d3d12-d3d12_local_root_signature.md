---
UID: NS:d3d12.D3D12_LOCAL_ROOT_SIGNATURE
title: D3D12_LOCAL_ROOT_SIGNATURE (d3d12.h)
description: Defines a local root signature state subobject that will be used with associated shaders.
helpviewer_keywords: ["D3D12_LOCAL_ROOT_SIGNATURE","D3D12_LOCAL_ROOT_SIGNATURE structure","PD3D12_LOCAL_ROOT_SIGNATURE","PD3D12_LOCAL_ROOT_SIGNATURE structure pointer","d3d12/D3D12_LOCAL_ROOT_SIGNATURE","d3d12/PD3D12_LOCAL_ROOT_SIGNATURE","direct3d12.d3d12_local_root_signature"]
old-location: direct3d12\d3d12_local_root_signature.htm
tech.root: direct3d12
ms.assetid: 98265867-4A2A-4AFC-B6B8-F91AC343C2B9
ms.date: 12/05/2018
ms.keywords: D3D12_LOCAL_ROOT_SIGNATURE, D3D12_LOCAL_ROOT_SIGNATURE structure, PD3D12_LOCAL_ROOT_SIGNATURE, PD3D12_LOCAL_ROOT_SIGNATURE structure pointer, d3d12/D3D12_LOCAL_ROOT_SIGNATURE, d3d12/PD3D12_LOCAL_ROOT_SIGNATURE, direct3d12.d3d12_local_root_signature
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
req.typenames: D3D12_LOCAL_ROOT_SIGNATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_LOCAL_ROOT_SIGNATURE
 - d3d12/D3D12_LOCAL_ROOT_SIGNATURE
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
 - D3D12_LOCAL_ROOT_SIGNATURE
---

# D3D12_LOCAL_ROOT_SIGNATURE structure


## -description

Defines a local root signature state subobject that will be used with associated shaders.

## -struct-fields

### -field pLocalRootSignature

The root signature that will function as a local root signature.  A state object holds a reference to this signature.

## -remarks

The presence of this subobject in a state object is optional.  The combination of global and/or local root signatures associated with any given shader function must define all resource bindings declared by the shader (with no overlap across global and local root signatures).

If any given function in a call graph (not counting calls across shader tables) is associated with a particular local root signature, any other functions in the graph must either be associated with the same local root signature or none, and the shader entry (the root of the call graph) must be associated with the local root signature.  This is due to the fact that the set of code reachable from a given shader entry gets invoked from a shader identifier in a shader record, where a single set of local root arguments apply.  Of course different shaders can use different local root signatures (or none), as their shader identifiers will be in different shader records.

