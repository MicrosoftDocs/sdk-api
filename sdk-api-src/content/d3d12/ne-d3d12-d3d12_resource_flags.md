---
UID: NE:d3d12.D3D12_RESOURCE_FLAGS
title: D3D12_RESOURCE_FLAGS (d3d12.h)
description: Specifies options for working with resources.
helpviewer_keywords: ["D3D12_RESOURCE_FLAGS","D3D12_RESOURCE_FLAGS enumeration","D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER","D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL","D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET","D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS","D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS","D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE","D3D12_RESOURCE_FLAG_NONE","D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY","d3d12/D3D12_RESOURCE_FLAGS","d3d12/D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER","d3d12/D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL","d3d12/D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET","d3d12/D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS","d3d12/D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS","d3d12/D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE","d3d12/D3D12_RESOURCE_FLAG_NONE","d3d12/D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY","direct3d12.d3d12_resource_flags"]
old-location: direct3d12\d3d12_resource_flags.htm
tech.root: direct3d12
ms.assetid: EC9DA05A-D0C0-4642-8E49-9ED98B4F19B4
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_FLAGS, D3D12_RESOURCE_FLAGS enumeration, D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER, D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL, D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET, D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS, D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE, D3D12_RESOURCE_FLAG_NONE, D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY, d3d12/D3D12_RESOURCE_FLAGS, d3d12/D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER, d3d12/D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL, d3d12/D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET, d3d12/D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS, d3d12/D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS, d3d12/D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE, d3d12/D3D12_RESOURCE_FLAG_NONE, d3d12/D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY, direct3d12.d3d12_resource_flags
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
req.typenames: D3D12_RESOURCE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESOURCE_FLAGS
 - d3d12/D3D12_RESOURCE_FLAGS
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
 - D3D12_RESOURCE_FLAGS
---

# D3D12_RESOURCE_FLAGS enumeration


## -description

Specifies options for working with resources.

## -enum-fields

### -field D3D12_RESOURCE_FLAG_NONE:0

No options are specified.

### -field D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET:0x1

Allows a render target view to be created for the resource, as well as enables the resource to transition into the state of D3D12_RESOURCE_STATE_RENDER_TARGET. Some adapter architectures allocate extra memory for textures with this flag to reduce the effective bandwidth during common rendering. This characteristic may not be beneficial for textures that are never rendered to, nor is it available for textures compressed with BC formats. Applications should avoid setting this flag when rendering will never occur.


The following restrictions and interactions apply:

<ul>
<li> Either the texture format must support render target capabilities at the current feature level. Or, when the format is a typeless format, a format within the same typeless group must support render target capabilities at the current feature level.</li>
<li>Cannot be set in conjunction with textures that have D3D12_TEXTURE_LAYOUT_ROW_MAJOR when <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>::<b>CrossAdapterRowMajorTextureSupported</b> is FALSE nor in conjunction with textures that have D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE when     <b>D3D12_FEATURE_DATA_D3D12_OPTIONS</b>::<b>StandardSwizzle64KBSupported</b> is FALSE.
</li>
<li>Cannot be used with 4KB alignment, D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL, nor usage with heaps that have D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES.</li>
</ul>

### -field D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL:0x2

Allows a depth stencil view to be created for the resource, as well as enables the resource to transition into the state of D3D12_RESOURCE_STATE_DEPTH_WRITE and/or D3D12_RESOURCE_STATE_DEPTH_READ. Most adapter architectures allocate extra memory for textures with this flag to reduce the effective bandwidth and maximize optimizations for early depth-test. Applications should avoid setting this flag when depth operations will never occur.


The following restrictions and interactions apply:

<ul>
<li>Either the texture format must support depth stencil capabilities at the current feature level. Or, when the format is a typeless format, a format within the same typeless group must support depth stencil capabilities at the current feature level.</li>
<li>Cannot be used with D3D12_RESOURCE_DIMENSION_BUFFER, 4KB alignment, D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS, D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS, D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE, D3D12_TEXTURE_LAYOUT_ROW_MAJOR, nor used with heaps that have D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES or D3D12_HEAP_FLAG_ALLOW_DISPLAY.
</li>
<li>Precludes usage of <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource">WriteToSubresource</a> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource">ReadFromSubresource</a>.
</li>
<li>Precludes GPU copying of a subregion. <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">CopyTextureRegion</a> must copy a whole subresource to or from resources with this flag.</li>
</ul>

### -field D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS:0x4

Allows an unordered access view to be created for the resource, as well as enables the resource to transition into the state of D3D12_RESOURCE_STATE_UNORDERED_ACCESS. Some adapter architectures must resort to less efficient texture layouts in order to provide this functionality. If a texture is rarely used for unordered access, it may be worth having two textures around and copying between them. One texture would have this flag, while the other wouldn't. Applications should avoid setting this flag when unordered access operations will never occur.


The following restrictions and interactions apply:

<ul>
<li>Either the texture format must support unordered access capabilities at the current feature level. Or, when the format is a typeless format, a format within the same typeless group must support unordered access capabilities at the current feature level.
</li>
<li>Cannot be set in conjunction with textures that have D3D12_TEXTURE_LAYOUT_ROW_MAJOR when <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>::<b>CrossAdapterRowMajorTextureSupported</b> is FALSE nor in conjunction with textures that have D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE when <b>D3D12_FEATURE_DATA_D3D12_OPTIONS</b>::<b>StandardSwizzle64KBSupported</b> is FALSE, nor when the feature level is less than 11.0.
</li>
<li>Cannot be used with MSAA textures. </li>
</ul>

### -field D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE:0x8

Disallows a shader resource view to be created for the resource, as well as disables the resource to transition into the state of D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE or D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE. Some adapter architectures experience increased bandwidth for depth stencil textures when shader resource views are precluded. If a texture is rarely used for shader resource, it may be worth having two textures around and copying between them. One texture would have this flag and the other wouldn't. Applications should set this flag when depth stencil textures will never be used from shader resource views.


The following restrictions and interactions apply:


<ul>
<li>Must be used with D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL. 
</li>
</ul>

### -field D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER:0x10

Allows the resource to be used for cross-adapter data, as well as the same features enabled by ALLOW_SIMULTANEOUS_ACCESS. Cross adapter resources commonly preclude techniques that reduce effective texture bandwidth during usage, and some adapter architectures may require different caching behavior. Applications should avoid setting this flag when the resource data will never be used with another adapter.

The following restrictions and interactions apply:


<ul>
<li>Must be used with heaps that have D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER.</li>
<li>Cannot be used with heaps that have D3D12_HEAP_FLAG_ALLOW_DISPLAY.</li>
</ul>

### -field D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS:0x20

Allows a resource to be simultaneously accessed by multiple different queues, devices or processes (for example, allows a resource to be used with <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier">ResourceBarrier</a> transitions performed in more than one command list 
	executing at the same time). 

Simultaneous access allows multiple readers and one writer, as long as the writer doesn't concurrently modify the texels that other readers are accessing. Some adapter architectures cannot leverage techniques to reduce effective texture bandwidth during usage. 

However, applications should avoid setting this flag when multiple readers are not required during frequent, non-overlapping writes to textures. Use of this flag can compromise resource fences to perform waits, and prevents any compression being used with a resource.

These restrictions and interactions apply.

- Can't be used with [D3D12_RESOURCE_DIMENSION_BUFFER](./ne-d3d12-d3d12_resource_dimension.md); but buffers always have the properties represented by this flag.
- Can't be used with MSAA textures.
- Can't be used with [D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL]().

### -field D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY:0x40

This resource may only be used as a decode reference frame.  It may only be written to or read by the video decode operation.  

[D3D12_VIDEO_DECODE_TIER_1](../d3d12video/ne-d3d12video-d3d12_video_decode_tier.md) and [D3D12_VIDEO_DECODE_TIER_2](../d3d12video/ne-d3d12video-d3d12_video_decode_tier.md) may report     [D3D12_VIDEO_DECODE_CONFIGURATION_FLAG_REFERENCE_ONLY_ALLOCATIONS_REQUIRED](../d3d12video/ne-d3d12video-d3d12_video_decode_configuration_flags.md) in the [D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT](../d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_support.md) structure configuration flag.  If so, the application must allocate reference frames with the new **D3D12\_RESOURCE\_VIDEO\_DECODE\_REFERENCE\_ONLY** resource flag.  [D3D12_VIDEO_DECODE_TIER_3](../d3d12video/ne-d3d12video-d3d12_video_decode_tier.md) must not set the [D3D12_VIDEO_DECODE_CONFIGURATION_FLAG_REFERENCE_ONLY_ALLOCATIONS_REQUIRED]
(../d3d12video/ne-d3d12video-d3d12_video_decode_configuration_flags)) configuration flag and must not require the use of this resource flag.

## -remarks

This enum is used by the <b>Flags</b> member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc">D3D12_RESOURCE_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
