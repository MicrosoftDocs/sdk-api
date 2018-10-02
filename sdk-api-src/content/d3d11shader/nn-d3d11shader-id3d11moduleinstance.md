---
UID: NN:d3d11shader.ID3D11ModuleInstance
title: ID3D11ModuleInstance
author: windows-sdk-content
description: A module-instance interface is used for resource rebinding.
old-location: direct3d11\id3d11moduleinstance.htm
tech.root: direct3d11
ms.assetid: BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11ModuleInstance, ID3D11ModuleInstance interface [Direct3D 11], ID3D11ModuleInstance interface [Direct3D 11],described, d3d11shader/ID3D11ModuleInstance, direct3d11.id3d11moduleinstance
ms.prod: windows
ms.technology: windows-sdk
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ModuleInstance</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D11ModuleInstance</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn280565(v=VS.85).aspx">BindConstantBuffer</a>
</td>
<td align="left" width="63%">
Rebinds a constant buffer from a source slot to a destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280566(v=VS.85).aspx">BindConstantBufferByName</a>
</td>
<td align="left" width="63%">
Rebinds a constant buffer by name to a destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280567(v=VS.85).aspx">BindResource</a>
</td>
<td align="left" width="63%">
Rebinds a texture or buffer from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280568(v=VS.85).aspx">BindResourceAsUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Rebinds a resource as an unordered access view (UAV) from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280569(v=VS.85).aspx">BindResourceAsUnorderedAccessViewByName</a>
</td>
<td align="left" width="63%">
Rebinds a resource by name as an unordered access view (UAV) to destination slots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280570(v=VS.85).aspx">BindResourceByName</a>
</td>
<td align="left" width="63%">
Rebinds a texture or buffer by name to destination slots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280571(v=VS.85).aspx">BindSampler</a>
</td>
<td align="left" width="63%">
Rebinds a sampler from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280605(v=VS.85).aspx">BindSamplerByName</a>
</td>
<td align="left" width="63%">
Rebinds a sampler by name to destination slots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280606(v=VS.85).aspx">BindUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Rebinds an unordered access view (UAV) from source slot to destination slot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280607(v=VS.85).aspx">BindUnorderedAccessViewByName</a>
</td>
<td align="left" width="63%">
Rebinds an unordered access view (UAV) by name to destination slots.

</td>
</tr>
</table> 


## -remarks



To get a module-instance interface, call <a href="https://msdn.microsoft.com/en-us/library/Dn280608(v=VS.85).aspx">ID3D11Module::CreateInstance</a> or <a href="https://msdn.microsoft.com/en-us/library/Dn280537(v=VS.85).aspx">ID3D11FunctionLinkingGraph::CreateModuleInstance</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11ModuleInstance</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476161(v=VS.85).aspx">Shader Interfaces</a>
 

 

