---
UID: NN:d3d11shader.ID3D11ModuleInstance
title: ID3D11ModuleInstance (d3d11shader.h)
description: A module-instance interface is used for resource rebinding.
old-location: direct3d11\id3d11moduleinstance.htm
tech.root: direct3d11
ms.assetid: BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5
ms.date: 12/05/2018
ms.keywords: ID3D11ModuleInstance, ID3D11ModuleInstance interface [Direct3D 11], ID3D11ModuleInstance interface [Direct3D 11],described, d3d11shader/ID3D11ModuleInstance, direct3d11.id3d11moduleinstance
f1_keywords:
- d3d11shader/ID3D11ModuleInstance
dev_langs:
- c++
req.header: d3d11shader.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3DCompiler_47.dll
api_name:
- ID3D11ModuleInstance
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11ModuleInstance interface


## -description


A module-instance interface is used for resource rebinding. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ModuleInstance</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ModuleInstance</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11ModuleInstance</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11moduleinstance-bindconstantbuffer">BindConstantBuffer</a>
</td>
<td align="left" width="63%">
Rebinds a constant buffer from a source slot to a destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11moduleinstance-bindconstantbufferbyname">BindConstantBufferByName</a>
</td>
<td align="left" width="63%">
Rebinds a constant buffer by name to a destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11moduleinstance-bindresource">BindResource</a>
</td>
<td align="left" width="63%">
Rebinds a texture or buffer from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11moduleinstance-bindresourceasunorderedaccessview">BindResourceAsUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Rebinds a resource as an unordered access view (UAV) from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11moduleinstance-bindresourceasunorderedaccessviewbyname">BindResourceAsUnorderedAccessViewByName</a>
</td>
<td align="left" width="63%">
Rebinds a resource by name as an unordered access view (UAV) to destination slots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11moduleinstance-bindresourcebyname">BindResourceByName</a>
</td>
<td align="left" width="63%">
Rebinds a texture or buffer by name to destination slots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11moduleinstance-bindsampler">BindSampler</a>
</td>
<td align="left" width="63%">
Rebinds a sampler from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11moduleinstance-bindsamplerbyname">BindSamplerByName</a>
</td>
<td align="left" width="63%">
Rebinds a sampler by name to destination slots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11moduleinstance-bindunorderedaccessview">BindUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Rebinds an unordered access view (UAV) from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11moduleinstance-bindunorderedaccessviewbyname">BindUnorderedAccessViewByName</a>
</td>
<td align="left" width="63%">
Rebinds an unordered access view (UAV) by name to destination slots.

</td>
</tr>
</table> 


## -remarks



To get a module-instance interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance">ID3D11Module::CreateInstance</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance">ID3D11FunctionLinkingGraph::CreateModuleInstance</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11ModuleInstance</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
 

 

