---
UID: NE:d3d12.D3D12_RESOURCE_FLAGS
title: D3D12_RESOURCE_FLAGS
author: windows-sdk-content
description: Specifies options for working with resources.
old-location: direct3d12\d3d12_resource_flags.htm
tech.root: direct3d12
ms.assetid: EC9DA05A-D0C0-4642-8E49-9ED98B4F19B4
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_RESOURCE_FLAGS, D3D12_RESOURCE_FLAGS enumeration, D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER, D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL, D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET, D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS, D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE, D3D12_RESOURCE_FLAG_NONE, D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY, d3d12/D3D12_RESOURCE_FLAGS, d3d12/D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER, d3d12/D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL, d3d12/D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET, d3d12/D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS, d3d12/D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS, d3d12/D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE, d3d12/D3D12_RESOURCE_FLAG_NONE, d3d12/D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY, direct3d12.d3d12_resource_flags
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D12_RESOURCE_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_RESOURCE_FLAGS
req.redist: 
---

# D3D12_RESOURCE_FLAGS enumeration


## -description


Specifies options for working with resources.
        


## -enum-fields




### -field D3D12_RESOURCE_FLAG_NONE

No options are specified.
          


### -field D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET

Allows a render target view to be created for the resource, as well as enables the resource to transition into the state of D3D12_RESOURCE_STATE_RENDER_TARGET. Some adapter architectures allocate extra memory for textures with this flag to reduce the effective bandwidth during common rendering. This characteristic may not be beneficial for textures that are never rendered to, nor is it available for textures compressed with BC formats. Applications should avoid setting this flag when rendering will never occur.


The following restrictions and interactions apply:

<ul>
<li> Either the texture format must support render target capabilities at the current feature level. Or, when the format is a typeless format, a format within the same typeless group must support render target capabilities at the current feature level.</li>
<li>Cannot be set in conjunction with textures that have D3D12_TEXTURE_LAYOUT_ROW_MAJOR when <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>::<b>CrossAdapterRowMajorTextureSupported</b> is FALSE nor in conjunction with textures that have D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE when     <b>D3D12_FEATURE_DATA_D3D12_OPTIONS</b>::<b>StandardSwizzle64KBSupported</b> is FALSE.
</li>
<li>Cannot be used with 4KB alignment, D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL, nor usage with heaps that have D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES.</li>
</ul>

### -field D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL

Allows a depth stencil view to be created for the resource, as well as enables the resource to transition into the state of D3D12_RESOURCE_STATE_DEPTH_WRITE and/or D3D12_RESOURCE_STATE_DEPTH_READ. Most adapter architectures allocate extra memory for textures with this flag to reduce the effective bandwidth and maximize optimizations for early depth-test. Applications should avoid setting this flag when depth operations will never occur.


The following restrictions and interactions apply:

<ul>
<li>Either the texture format must support depth stencil capabilities at the current feature level. Or, when the format is a typeless format, a format within the same typeless group must support depth stencil capabilities at the current feature level.</li>
<li>Cannot be used with D3D12_RESOURCE_DIMENSION_BUFFER, 4KB alignment, D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS, D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS, D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE, D3D12_TEXTURE_LAYOUT_ROW_MAJOR, nor used with heaps that have D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES or D3D12_HEAP_FLAG_ALLOW_DISPLAY.
</li>
<li>Precludes usage of <a href="https://msdn.microsoft.com/8781E2FE-8D82-41F5-B541-A96DA11CA290">WriteToSubresource</a> and <a href="https://msdn.microsoft.com/A1F61217-A383-49BF-B675-FBC7F6D015DB">ReadFromSubresource</a>.
</li>
<li>Precludes GPU copying of a subregion. <a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">CopyTextureRegion</a> must copy a whole subresource to or from resources with this flag.</li>
</ul>

### -field D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS

Allows an unordered access view to be created for the resource, as well as enables the resource to transition into the state of D3D12_RESOURCE_STATE_UNORDERED_ACCESS. Some adapter architectures must resort to less efficient texture layouts in order to provide this functionality. If a texture is rarely used for unordered access, it may be worth having two textures around and copying between them. One texture would have this flag, while the other wouldn't. Applications should avoid setting this flag when unordered access operations will never occur.


The following restrictions and interactions apply:

<ul>
<li>Either the texture format must support unordered access capabilities at the current feature level. Or, when the format is a typeless format, a format within the same typeless group must support unordered access capabilities at the current feature level.
</li>
<li>Cannot be set in conjunction with textures that have D3D12_TEXTURE_LAYOUT_ROW_MAJOR when <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>::<b>CrossAdapterRowMajorTextureSupported</b> is FALSE nor in conjunction with textures that have D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE when <b>D3D12_FEATURE_DATA_D3D12_OPTIONS</b>::<b>StandardSwizzle64KBSupported</b> is FALSE, nor when the feature level is less than 11.0.
</li>
<li>Cannot be used with MSAA textures. </li>
</ul>

### -field D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE

Disallows a shader resource view to be created for the resource, as well as disables the resource to transition into the state of D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE or D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE. Some adapter architectures experience increased bandwidth for depth stencil textures when shader resource views are precluded. If a texture is rarely used for shader resource, it may be worth having two textures around and copying between them. One texture would have this flag and the other wouldn't. Applications should set this flag when depth stencil textures will never be used from shader resource views.


The following restrictions and interactions apply:


<ul>
<li>Must be used with D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL. 
</li>
</ul>

### -field D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER

Allows the resource to be used for cross-adapter data, as well as the same features enabled by ALLOW_SIMULTANEOUS_ACCESS. Cross adapter resources commonly preclude techniques that reduce effective texture bandwidth during usage, and some adapter architectures may require different caching behavior. Applications should avoid setting this flag when the resource data will never be used with another adapter.

The following restrictions and interactions apply:


<ul>
<li>Must be used with heaps that have D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER.</li>
<li>Cannot be used with heaps that have D3D12_HEAP_FLAG_ALLOW_DISPLAY.</li>
</ul>

### -field D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS

Allows a resource to be simultaneously accessed by multiple different queues, devices or processes (for example, allows a resource to be used with <a href="https://msdn.microsoft.com/AA788F94-122B-4132-BED5-162EAC683676">ResourceBarrier</a> transitions performed in more than one command list 
	executing at the same time). 

Simultaneous access allows multiple readers and one writer, as long as the writer doesn't concurrently modify the texels that other readers are accessing. Some adapter architectures cannot leverage techniques to reduce effective texture bandwidth during usage. 

However, applications should avoid setting this flag when multiple readers are not required during frequent, non-overlapping writes to textures. Use of this flag can compromise resource fences to perform waits, and prevents any compression being used with a resource.

The following restrictions and interactions apply:


<ul>
<li>Cannot be used with D3D12_RESOURCE_DIMENSION_BUFFER; but buffers always have the properties represented by this flag.
</li>
<li>Cannot be used with MSAA textures.</li>
</ul>

### -field D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY


## -remarks



This enum is used by the <b>Flags</b> member of the <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a> structure.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

