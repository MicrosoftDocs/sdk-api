---
UID: NN:d3d12shader.ID3D12ShaderReflection
title: ID3D12ShaderReflection (d3d12shader.h)
author: windows-sdk-content
description: A shader-reflection interface accesses shader information.
old-location: direct3d12\id3d12shaderreflection.htm
tech.root: direct3d12
ms.assetid: 145F2CCB-C076-42BE-8AF4-74349CDF6B02
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12ShaderReflection, ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,described, d3d12shader/ID3D12ShaderReflection, direct3d12.id3d12shaderreflection
ms.topic: interface
f1_keywords: 
 - "d3d12shader/ID3D12ShaderReflection"
dev_langs:
 - c++
req.header: d3d12shader.h
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
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12ShaderReflection interface


## -description


A shader-reflection interface accesses shader information.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12ShaderReflection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12ShaderReflection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12ShaderReflection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getbitwiseinstructioncount">GetBitwiseInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of bitwise instructions.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getconstantbufferbyindex">GetConstantBufferByIndex</a>
</td>
<td align="left" width="63%">
Gets a constant buffer by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getconstantbufferbyname">GetConstantBufferByName</a>
</td>
<td align="left" width="63%">
Gets a constant buffer by name.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getconversioninstructioncount">GetConversionInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of conversion instructions.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a shader description.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getgsinputprimitive">GetGSInputPrimitive</a>
</td>
<td align="left" width="63%">
Gets the geometry-shader input-primitive description.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getinputparameterdesc">GetInputParameterDesc</a>
</td>
<td align="left" width="63%">
Gets an input-parameter description for a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getminfeaturelevel">GetMinFeatureLevel</a>
</td>
<td align="left" width="63%">
Gets the minimum feature level.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getmovcinstructioncount">GetMovcInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Movc instructions.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getmovinstructioncount">GetMovInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Mov instructions.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getnuminterfaceslots">GetNumInterfaceSlots</a>
</td>
<td align="left" width="63%">
Gets the number of interface slots in a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getoutputparameterdesc">GetOutputParameterDesc</a>
</td>
<td align="left" width="63%">
Gets an output-parameter description for a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getpatchconstantparameterdesc">GetPatchConstantParameterDesc</a>
</td>
<td align="left" width="63%">
Gets a patch-constant parameter description for a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getrequiresflags">GetRequiresFlags</a>
</td>
<td align="left" width="63%">
Gets a group of flags that indicates the requirements of a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getresourcebindingdesc">GetResourceBindingDesc</a>
</td>
<td align="left" width="63%">
Gets a description of how a resource is bound to a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getresourcebindingdescbyname">GetResourceBindingDescByName</a>
</td>
<td align="left" width="63%">
Gets a description of how a resource is bound to a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getthreadgroupsize">GetThreadGroupSize</a>
</td>
<td align="left" width="63%">
Retrieves the sizes, in units of threads, of the X, Y, and Z dimensions of the shader's thread-group grid.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getvariablebyname">GetVariableByName</a>
</td>
<td align="left" width="63%">
Gets a variable by name.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-issamplefrequencyshader">IsSampleFrequencyShader</a>
</td>
<td align="left" width="63%">
Indicates whether a shader is a sample frequency shader.
        

</td>
</tr>
</table> 


## -remarks



An <b>ID3D12ShaderReflection</b> interface can be retrieved for a shader by using 
				<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/d3dreflect">D3DReflect</a>.  
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
 

 

