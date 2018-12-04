---
UID: NE:d3d12.D3D12_RAY_FLAGS
title: D3D12_RAY_FLAGS
author: windows-sdk-content
description: Flags passed to the TraceRay function to override transparency, culling, and early-out behavior.
old-location: direct3d12\d3d12_ray_flags.htm
tech.root: direct3d12
ms.assetid: AD2494F6-AF2E-46E8-9140-2E91BD2BA3EB
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: D3D12_RAY_FLAGS, D3D12_RAY_FLAGS enumeration, D3D12_RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH, D3D12_RAY_FLAG_CULL_BACK_FACING_TRIANGLES, D3D12_RAY_FLAG_CULL_FRONT_FACING_TRIANGLES, D3D12_RAY_FLAG_CULL_NON_OPAQUE, D3D12_RAY_FLAG_CULL_OPAQUE, D3D12_RAY_FLAG_FORCE_NON_OPAQUE, D3D12_RAY_FLAG_FORCE_OPAQUE, D3D12_RAY_FLAG_NONE, D3D12_RAY_FLAG_SKIP_CLOSEST_HIT_SHADER, d3d12/D3D12_RAY_FLAGS, d3d12/D3D12_RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH, d3d12/D3D12_RAY_FLAG_CULL_BACK_FACING_TRIANGLES, d3d12/D3D12_RAY_FLAG_CULL_FRONT_FACING_TRIANGLES, d3d12/D3D12_RAY_FLAG_CULL_NON_OPAQUE, d3d12/D3D12_RAY_FLAG_CULL_OPAQUE, d3d12/D3D12_RAY_FLAG_FORCE_NON_OPAQUE, d3d12/D3D12_RAY_FLAG_FORCE_OPAQUE, d3d12/D3D12_RAY_FLAG_NONE, d3d12/D3D12_RAY_FLAG_SKIP_CLOSEST_HIT_SHADER, direct3d12.d3d12_ray_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_RAY_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_RAY_FLAGS
req.redist: 
---

# D3D12_RAY_FLAGS enumeration


## -description


Flags passed to the <a href="https://docs.microsoft.com/en-us/windows/desktop/direct3d12/traceray-function">TraceRay</a> function to override transparency, culling, and early-out behavior.


## -enum-fields




### -field D3D12_RAY_FLAG_NONE

No options selected.


### -field D3D12_RAY_FLAG_FORCE_OPAQUE

All ray-primitive intersections encountered in a raytrace are treated as opaque. So no any hit shaders will be executed regardless of whether or not the hit geometry specifies D3D12_RAYTRACING_GEOMETRY_FLAG_OPAQUE, and regardless of the instance flags on the instance that was hit.

This flag is mutually exclusive with RAY_FLAG_FORCE_NON_OPAQUE, RAY_FLAG_CULL_OPAQUE and RAY_FLAG_CULL_NON_OPAQUE.


### -field D3D12_RAY_FLAG_FORCE_NON_OPAQUE

All ray-primitive intersections encountered in a raytrace are treated as non-opaque. So any hit shaders, if present, will be executed regardless of whether or not the hit geometry specifies D3D12_RAYTRACING_GEOMETRY_FLAG_OPAQUE, and regardless of the instance flags on the instance that was hit. This flag is mutually exclusive with RAY_FLAG_FORCE_\OPAQUE, RAY_FLAG_CULL_OPAQUE and RAY_FLAG_CULL_NON_OPAQUE.


### -field D3D12_RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH

The first ray-primitive intersection encountered in a raytrace automatically causes <a href="https://docs.microsoft.com/en-us/windows/desktop/direct3d12/accepthitandendsearch-function">AcceptHitAndEndSearch</a> to be called immediately after the any hit shader, including if there is no any hit shader.

The only exception is when the preceding any hit shader calls <a href="https://docs.microsoft.com/en-us/windows/desktop/direct3d12/ignorehit-function">IgnoreHit</a>, in which case the ray continues unaffected such that the next hit becomes another candidate to be the first hit. For this exception to apply, the any hit shader has to actually be executed. So if the any hit shader is skipped because the hit is treated as opaque (e.g. due to RAY_FLAG_FORCE_OPAQUE or D3D12_RAYTRACING_GEOMETRY_FLAG_OPAQUE or D3D12_RAYTRACING_INSTANCE_FLAG_OPAQUE being set), then <b>AcceptHitAndEndSearch</b> is called.

If a closest hit shader is present at the first hit, it gets invoked unless RAY_FLAG_SKIP_CLOSEST_HIT_SHADER is also present. The one hit that was found is considered “closest”, even though other potential hits that might be closer on the ray may not have been visited.

A typical use for this flag is for shadows, where only a single hit needs to be found.


### -field D3D12_RAY_FLAG_SKIP_CLOSEST_HIT_SHADER

Even if at least one hit has been committed, and the hit group for the closest hit contains a closest hit shader, skip execution of that shader.


### -field D3D12_RAY_FLAG_CULL_BACK_FACING_TRIANGLES

Enables culling of back facing triangles. See <a href="https://msdn.microsoft.com/418D1EF1-FC41-4BEF-914E-A9C82E78567A">D3D12_RAYTRACING_INSTANCE_FLAGS</a> for selecting which triangles are back facing, per-instance.

On instances that specify D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_CULL_DISABLE, this flag has no effect.

On geometry types other than D3D12_RAYTRACING_GEOMETRY_TYPE_TRIANGLES, this flag has no effect.

This flag is mutually exclusive with RAY_FLAG_CULL_FRONT_FACING_TRIANGLES.


### -field D3D12_RAY_FLAG_CULL_FRONT_FACING_TRIANGLES

Enables culling of front facing triangles. See <a href="https://msdn.microsoft.com/418D1EF1-FC41-4BEF-914E-A9C82E78567A">D3D12_RAYTRACING_INSTANCE_FLAGS</a> for selecting which triangles are back facing, per-instance.

On instances that specify D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_CULL_DISABLE, this flag has no effect.

On geometry types other than D3D12_RAYTRACING_GEOMETRY_TYPE_TRIANGLES, this flag has no effect.

This flag is mutually exclusive with RAY_FLAG_CULL_FRONT_FACING_TRIANGLES.


### -field D3D12_RAY_FLAG_CULL_OPAQUE

Culls all primitives that are considered opaque based on their geometry and instance flags.

This flag is mutually exclusive with RAY_FLAG_FORCE_OPAQUE, RAY_FLAG_FORCE_NON_OPAQUE, and RAY_FLAG_CULL_NON_OPAQUE.


### -field D3D12_RAY_FLAG_CULL_NON_OPAQUE

Culls all primitives that are considered non-opaque based on their geometry and instance flags.

This flag is mutually exclusive with RAY_FLAG_FORCE_OPAQUE, RAY_FLAG_FORCE_NON_OPAQUE, and RAY_FLAG_CULL_OPAQUE.

