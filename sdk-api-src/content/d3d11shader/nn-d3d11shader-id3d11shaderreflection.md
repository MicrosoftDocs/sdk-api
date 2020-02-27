---
UID: NN:d3d11shader.ID3D11ShaderReflection
title: ID3D11ShaderReflection (d3d11shader.h)
description: A shader-reflection interface accesses shader information.
old-location: direct3d11\id3d11shaderreflection.htm
tech.root: direct3d11
ms.assetid: a28cca72-7f2d-416a-bfa9-4d1f71fc98d5
ms.date: 12/05/2018
ms.keywords: 83fba8f9-987e-26d3-4909-fd45ac6e9df2, ID3D11ShaderReflection, ID3D11ShaderReflection interface [Direct3D 11], ID3D11ShaderReflection interface [Direct3D 11],described, d3d11shader/ID3D11ShaderReflection, direct3d11.id3d11shaderreflection
f1_keywords:
- d3d11shader/ID3D11ShaderReflection
dev_langs:
- c++
req.header: d3d11shader.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
- ID3D11ShaderReflection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11ShaderReflection interface


## -description


A shader-reflection interface accesses shader information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderReflection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ShaderReflection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11ShaderReflection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getbitwiseinstructioncount">GetBitwiseInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of bitwise instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getconstantbufferbyindex">GetConstantBufferByIndex</a>
</td>
<td align="left" width="63%">
Get a constant buffer by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getconstantbufferbyname">GetConstantBufferByName</a>
</td>
<td align="left" width="63%">
Get a constant buffer by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getconversioninstructioncount">GetConversionInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of conversion instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getgsinputprimitive">GetGSInputPrimitive</a>
</td>
<td align="left" width="63%">
Gets the geometry-shader input-primitive description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getinputparameterdesc">GetInputParameterDesc</a>
</td>
<td align="left" width="63%">
Get an input-parameter description for a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getminfeaturelevel">GetMinFeatureLevel</a>
</td>
<td align="left" width="63%">
Gets the minimum feature level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getmovcinstructioncount">GetMovcInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Movc instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getmovinstructioncount">GetMovInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Mov instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots">GetNumInterfaceSlots</a>
</td>
<td align="left" width="63%">
Gets the number of interface slots in a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getoutputparameterdesc">GetOutputParameterDesc</a>
</td>
<td align="left" width="63%">
Get an output-parameter description for a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getpatchconstantparameterdesc">GetPatchConstantParameterDesc</a>
</td>
<td align="left" width="63%">
Get a patch-constant parameter description for a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getrequiresflags">GetRequiresFlags</a>
</td>
<td align="left" width="63%">
Gets a group of flags that indicates the requirements of a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getresourcebindingdesc">GetResourceBindingDesc</a>
</td>
<td align="left" width="63%">
Get a description of how a resource is bound to a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getresourcebindingdescbyname">GetResourceBindingDescByName</a>
</td>
<td align="left" width="63%">
Get a description of how a resource is bound to a shader. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getthreadgroupsize">GetThreadGroupSize</a>
</td>
<td align="left" width="63%">
Retrieves the sizes, in units of threads, of the X, Y, and Z dimensions of the shader's thread-group grid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname">GetVariableByName</a>
</td>
<td align="left" width="63%">
Gets a variable by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader">IsSampleFrequencyShader</a>
</td>
<td align="left" width="63%">
Indicates whether a shader is a sample frequency shader.

</td>
</tr>
</table> 


## -remarks



An <b>ID3D11ShaderReflection</b> interface can be retrieved for a shader by using  <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/d3dreflect">D3DReflect</a>.  The following code illustrates retrieving a <b>ID3D11ShaderReflection</b>  from a shader.
          


```
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3DReflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            IID_ID3D11ShaderReflection, (void**) &pReflector);
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
 

 

