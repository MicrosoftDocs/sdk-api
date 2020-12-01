---
UID: NS:d3d12.D3D12_GLOBAL_ROOT_SIGNATURE
title: D3D12_GLOBAL_ROOT_SIGNATURE (d3d12.h)
description: Defines a global root signature state suboject that will be used with associated shaders.
helpviewer_keywords: ["D3D12_GLOBAL_ROOT_SIGNATURE","D3D12_GLOBAL_ROOT_SIGNATURE structure","PD3D12_GLOBAL_ROOT_SIGNATURE","PD3D12_GLOBAL_ROOT_SIGNATURE structure pointer","d3d12/D3D12_GLOBAL_ROOT_SIGNATURE","d3d12/PD3D12_GLOBAL_ROOT_SIGNATURE","direct3d12.d3d12_global_root_signature"]
old-location: direct3d12\d3d12_global_root_signature.htm
tech.root: direct3d12
ms.assetid: 971433E7-9221-4988-BAD9-2DD1D14A5039
ms.date: 12/05/2018
ms.keywords: D3D12_GLOBAL_ROOT_SIGNATURE, D3D12_GLOBAL_ROOT_SIGNATURE structure, PD3D12_GLOBAL_ROOT_SIGNATURE, PD3D12_GLOBAL_ROOT_SIGNATURE structure pointer, d3d12/D3D12_GLOBAL_ROOT_SIGNATURE, d3d12/PD3D12_GLOBAL_ROOT_SIGNATURE, direct3d12.d3d12_global_root_signature
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
req.typenames: D3D12_GLOBAL_ROOT_SIGNATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_GLOBAL_ROOT_SIGNATURE
 - d3d12/D3D12_GLOBAL_ROOT_SIGNATURE
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
 - D3D12_GLOBAL_ROOT_SIGNATURE
---

# D3D12_GLOBAL_ROOT_SIGNATURE structure


## -description

Defines a global root signature state suboject that will be used with associated shaders.

## -struct-fields

### -field pGlobalRootSignature

The root signature that will function as a global root signature.  A state object holds a reference to this signature.

## -remarks

The presence of this subobject in a state object is optional.  The combination of global and/or local root signatures associated with any given shader function must define all resource bindings declared by the shader with no overlap across global and local root signatures.

If any given function in a call graph is associated with a particular global root signature, any other functions in the graph must either be associated with the same global root signature or none, and the shader entry (the root of the call graph) must be associated with the global root signature.

Different shaders can use different global root signatures (or none) within a state object, however any shaders referenced during a particular <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays">DispatchRays</a> operation from a command list must have specified the same global root signature as what has been set on the command list as the compute root signature.  So it is valid to define a single large state object with multiple global root signatures associated with different subsets of the shaders. Apps are not forced to split their state object just because some shaders use different global root signatures.