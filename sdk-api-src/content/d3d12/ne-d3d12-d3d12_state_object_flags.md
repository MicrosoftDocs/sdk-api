---
UID: NE:d3d12.D3D12_STATE_OBJECT_FLAGS
title: D3D12_STATE_OBJECT_FLAGS (d3d12.h)
description: Specifies constraints for state objects. Use values from this enumeration in the D3D12_STATE_OBJECT_CONFIG structure.
helpviewer_keywords: ["D3D12_STATE_OBJECT_FLAGS","D3D12_STATE_OBJECT_FLAGS enumeration","D3D12_STATE_OBJECT_FLAG_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS","D3D12_STATE_OBJECT_FLAG_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITIONS","D3D12_STATE_OBJECT_FLAG_NONE","d3d12/ D3D12_STATE_OBJECT_FLAG_NONE","d3d12/D3D12_STATE_OBJECT_FLAGS","d3d12/D3D12_STATE_OBJECT_FLAG_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS","d3d12/D3D12_STATE_OBJECT_FLAG_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITIONS","direct3d12.d3d12_state_object_flags"]
old-location: direct3d12\d3d12_state_object_flags.htm
tech.root: direct3d12
ms.assetid: 735414B3-73FA-4063-81A2-92658D3D8CB2
ms.date: 12/05/2018
ms.keywords: D3D12_STATE_OBJECT_FLAGS, D3D12_STATE_OBJECT_FLAGS enumeration, D3D12_STATE_OBJECT_FLAG_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS, D3D12_STATE_OBJECT_FLAG_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITIONS, D3D12_STATE_OBJECT_FLAG_NONE, d3d12/ D3D12_STATE_OBJECT_FLAG_NONE, d3d12/D3D12_STATE_OBJECT_FLAGS, d3d12/D3D12_STATE_OBJECT_FLAG_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS, d3d12/D3D12_STATE_OBJECT_FLAG_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITIONS, direct3d12.d3d12_state_object_flags
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
req.typenames: D3D12_STATE_OBJECT_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_STATE_OBJECT_FLAGS
 - d3d12/D3D12_STATE_OBJECT_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_STATE_OBJECT_FLAGS
---

# D3D12_STATE_OBJECT_FLAGS enumeration


## -description

Specifies constraints for state objects. Use values from this enumeration in the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_state_object_config">D3D12_STATE_OBJECT_CONFIG</a> structure.

## -enum-fields

### -field D3D12_STATE_OBJECT_FLAG_NONE:0

No state object constraints.

### -field D3D12_STATE_OBJECT_FLAG_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITIONS:0x1

This flag applies to state objects of type collection only. Otherwise this flag is ignored.  

The exports from this collection are allowed to have unresolved references (dependencies) that would have to be resolved (defined) when the collection is included in a containing state object, such as a raytracing pipeline state object (RTPSO).  This includes depending on externally defined subobject associations to associate an external subobject (e.g. root signature) to a local export.

In the absence of this flag, all exports in this collection must have their dependencies fully locally resolved, including any necessary subobject associations being defined locally.  Advanced implementations/drivers will have enough information to compile the code in the collection and not need to keep around any uncompiled code (unless the <b>D3D12_STATE_OBJECT_FLAG_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</b> flag is set), so that when the collection is used in a containing state object (e.g. RTPSO), minimal work needs to be done by the driver, ideally a “cheap” link at most.

### -field D3D12_STATE_OBJECT_FLAG_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS:0x2

This flag applies to state objects of type collection only. Otherwise this flag is ignored.  

If this collection is included in another state object (e.g. RTPSO), shaders / functions in the rest of the containing state object are allowed to depend on (e.g. call) exports from this collection.

In the absence of this flag (default), exports from this collection cannot be directly referenced by other parts of containing state objects (e.g. RTPSO).  This can reduce memory footprint for the collection slightly since drivers don’t need to keep uncompiled code in the collection on the off chance that it may get called by some external function that would then compile all the code together.  That said, if not all necessary subobject associations have been locally defined for code in this collection, the driver may not be able to compile shader code yet and may still need to keep uncompiled code around.  

A subobject association defined externally that associates an external subobject to a local export does not count as an external dependency on a local definition, so the presence or absence of this flag does not affect whether the association is allowed or not. On the other hand if the current collection defines a subobject association for a locally defined subobject to an external export (e.g. shader), that counts as an external dependency on a local definition and this flag must be set.

Regardless of the presence or absence of this flag, shader entrypoints (such as hit groups or miss shaders) in the collection are visible as entrypoints to a containing state object (e.g. RTPSO) if exported by it.  In the case of an RTPSO, the exported entrypoints can be used in shader tables for raytracing.
