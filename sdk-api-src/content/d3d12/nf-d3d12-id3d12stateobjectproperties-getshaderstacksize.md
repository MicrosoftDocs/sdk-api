---
UID: NF:d3d12.ID3D12StateObjectProperties.GetShaderStackSize
title: ID3D12StateObjectProperties::GetShaderStackSize (d3d12.h)
description: Gets the amount of stack memory required to invoke a raytracing shader in HLSL.
helpviewer_keywords: ["GetShaderStackSize","GetShaderStackSize method","GetShaderStackSize method","ID3D12StateObjectProperties interface","ID3D12StateObjectProperties interface","GetShaderStackSize method","ID3D12StateObjectProperties.GetShaderStackSize","ID3D12StateObjectProperties::GetShaderStackSize","d3d12/ID3D12StateObjectProperties::GetShaderStackSize","direct3d12.id3d12stateobjectproperties_getshaderstacksize"]
old-location: direct3d12\id3d12stateobjectproperties_getshaderstacksize.htm
tech.root: direct3d12
ms.assetid: 3C804CAF-7263-4E37-9C00-F85959CE651D
ms.date: 12/05/2018
ms.keywords: GetShaderStackSize, GetShaderStackSize method, GetShaderStackSize method,ID3D12StateObjectProperties interface, ID3D12StateObjectProperties interface,GetShaderStackSize method, ID3D12StateObjectProperties.GetShaderStackSize, ID3D12StateObjectProperties::GetShaderStackSize, d3d12/ID3D12StateObjectProperties::GetShaderStackSize, direct3d12.id3d12stateobjectproperties_getshaderstacksize
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12StateObjectProperties::GetShaderStackSize
 - d3d12/ID3D12StateObjectProperties::GetShaderStackSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12StateObjectProperties.GetShaderStackSize
---

# ID3D12StateObjectProperties::GetShaderStackSize


## -description

Gets the amount of stack memory required to invoke a raytracing shader in HLSL.

## -parameters

### -param pExportName

The shader entrypoint in the state object for which to retrieve stack size.  For hit groups, an individual shader within the hit group must be specified using the syntax:

hitGroupName::shaderType

Where <i>hitGroupName</i> is the entrypoint name for the hit group and <i>shaderType</i> is one of: 

<ul>
<li>intersection</li>
<li>anyhit</li>
<li>closesthit</li>
</ul>
These values are all case-sensitive.

An example value is: "myTreeLeafHitGroup::anyhit".

## -returns

Amount of stack memory, in bytes, required to invoke the shader.  If the shader isn’t fully resolved in the state object, or the shader is unknown or of a type for which a stack size isn’t relevant, such as a hit group, the return value is 0xffffffff.  The 32-bit 0xffffffff value is used  for the UINT64 return value to ensure that bad return values don’t get lost when summed up with other values as part of calculating an overall pipeline stack size.

## -remarks

This method only needs to be called if the app wants to configure the stack size by calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12stateobjectproperties-setpipelinestacksize">SetPipelineStackSize</a>, rather than relying on the conservative default stack size. This method is only valid for ray generation shaders, hit groups, miss shaders, and callable shaders. Even ray generation shaders may return a non-zero value despite being at the bottom of the stack.

For hit groups, stack size must be queried for the individual shaders comprising it (intersection shaders, any hit shaders, closest hit shaders), as each likely has a different stack size requirement.  The stack size can’t be queried on these individual shaders directly, as the way they are compiled can be influenced by the overall hit group that contains them.  The <i>pExportName</i> parameter includes syntax for identifying individual shaders within a hit group.

This API can be called on either collection state objects or raytracing pipeline state objects.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12stateobjectproperties.md">ID3D12StateObjectProperties</a>
