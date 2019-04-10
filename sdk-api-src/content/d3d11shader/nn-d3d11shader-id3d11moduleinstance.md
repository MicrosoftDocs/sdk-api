---
UID: NN:d3d11shader.ID3D11ModuleInstance
title: ID3D11ModuleInstance (d3d11shader.h)
author: windows-sdk-content
description: A module-instance interface is used for resource rebinding.
old-location: direct3d11\id3d11moduleinstance.htm
tech.root: direct3d11
ms.assetid: BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11ModuleInstance, ID3D11ModuleInstance interface [Direct3D 11], ID3D11ModuleInstance interface [Direct3D 11],described, d3d11shader/ID3D11ModuleInstance, direct3d11.id3d11moduleinstance
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ModuleInstance interface


## -description


A module-instance interface is used for resource rebinding. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ModuleInstance</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11ModuleInstance</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/F12B8580-6D47-4C73-8281-287A0B183D7F">BindConstantBuffer</a>
</td>
<td align="left" width="63%">
Rebinds a constant buffer from a source slot to a destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ACC4A9C6-8B6A-4923-A51E-66AB423F12D5">BindConstantBufferByName</a>
</td>
<td align="left" width="63%">
Rebinds a constant buffer by name to a destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7EBF623B-1C04-43C5-A262-62EA125D6631">BindResource</a>
</td>
<td align="left" width="63%">
Rebinds a texture or buffer from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A9E61E17-F1FE-4BF1-8A4A-F73B23FEDD08">BindResourceAsUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Rebinds a resource as an unordered access view (UAV) from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B9A9BA35-7CAB-411D-8168-B126CB8C3139">BindResourceAsUnorderedAccessViewByName</a>
</td>
<td align="left" width="63%">
Rebinds a resource by name as an unordered access view (UAV) to destination slots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/313A4AE8-8B3A-40B9-85C4-86A43F4F37D5">BindResourceByName</a>
</td>
<td align="left" width="63%">
Rebinds a texture or buffer by name to destination slots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FB7A63DE-C8EC-456D-84D6-D0AF682A46E8">BindSampler</a>
</td>
<td align="left" width="63%">
Rebinds a sampler from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3AB143F9-6AF7-4C1A-8330-AAA4A7723327">BindSamplerByName</a>
</td>
<td align="left" width="63%">
Rebinds a sampler by name to destination slots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2948964B-73B1-4656-8547-F5238C3DC928">BindUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Rebinds an unordered access view (UAV) from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/439C12FD-4BAE-4609-88D3-D7B006816716">BindUnorderedAccessViewByName</a>
</td>
<td align="left" width="63%">
Rebinds an unordered access view (UAV) by name to destination slots.

</td>
</tr>
</table> 


## -remarks



To get a module-instance interface, call <a href="https://msdn.microsoft.com/737A69EF-F74E-4480-98EA-31D6CCAC0F8A">ID3D11Module::CreateInstance</a> or <a href="https://msdn.microsoft.com/7E854D31-3E34-43A7-ABEB-7FBAC94217F3">ID3D11FunctionLinkingGraph::CreateModuleInstance</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11ModuleInstance</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

