---
UID: NN:d3d11shader.ID3D11ShaderReflection
title: ID3D11ShaderReflection
author: windows-sdk-content
description: A shader-reflection interface accesses shader information.
old-location: direct3d11\id3d11shaderreflection.htm
tech.root: direct3d11
ms.assetid: a28cca72-7f2d-416a-bfa9-4d1f71fc98d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 83fba8f9-987e-26d3-4909-fd45ac6e9df2, ID3D11ShaderReflection, ID3D11ShaderReflection interface [Direct3D 11], ID3D11ShaderReflection interface [Direct3D 11],described, d3d11shader/ID3D11ShaderReflection, direct3d11.id3d11shaderreflection
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderReflection interface


## -description


A shader-reflection interface accesses shader information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderReflection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11ShaderReflection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/095fc6e0-972a-43d1-9738-16d7f0846e26">GetBitwiseInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of bitwise instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a1be6a0-0337-408d-9e31-8dd388faaf5d">GetConstantBufferByIndex</a>
</td>
<td align="left" width="63%">
Get a constant buffer by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b0e16c9-f45a-42d0-bd96-32dfa859b35d">GetConstantBufferByName</a>
</td>
<td align="left" width="63%">
Get a constant buffer by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4876bcc8-44b6-4e26-9f0e-cd915b39acb8">GetConversionInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of conversion instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88bebd52-5da0-473e-8f26-63a82ce99938">GetDesc</a>
</td>
<td align="left" width="63%">
Get a shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df34dc7e-e6aa-442d-905e-4ae11b62a781">GetGSInputPrimitive</a>
</td>
<td align="left" width="63%">
Gets the geometry-shader input-primitive description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6483634d-6050-4218-98ee-a7062efcbe64">GetInputParameterDesc</a>
</td>
<td align="left" width="63%">
Get an input-parameter description for a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b10eb64b-18ff-4248-be6e-a9c45bce3e99">GetMinFeatureLevel</a>
</td>
<td align="left" width="63%">
Gets the minimum feature level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b732d024-cc94-4292-ad11-e51b5d9328ff">GetMovcInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Movc instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de12c547-90a8-48c5-911a-3b0c91001038">GetMovInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Mov instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2182f64-0d0e-4b1c-a566-f33fe7a0b093">GetNumInterfaceSlots</a>
</td>
<td align="left" width="63%">
Gets the number of interface slots in a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fc27fae-d17a-4247-bd79-e02956890efd">GetOutputParameterDesc</a>
</td>
<td align="left" width="63%">
Get an output-parameter description for a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91a1a3ac-1dd4-4d91-aaea-196a99d5d684">GetPatchConstantParameterDesc</a>
</td>
<td align="left" width="63%">
Get a patch-constant parameter description for a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BC70E68A-8909-42F9-9AEE-017BA682D635">GetRequiresFlags</a>
</td>
<td align="left" width="63%">
Gets a group of flags that indicates the requirements of a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bd540f5-513d-4dd5-ab28-b0e8083231eb">GetResourceBindingDesc</a>
</td>
<td align="left" width="63%">
Get a description of how a resource is bound to a shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4bddcc0-c2fd-4dac-b999-cfbe1d318777">GetResourceBindingDescByName</a>
</td>
<td align="left" width="63%">
Get a description of how a resource is bound to a shader. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3f7b22d-75d6-4169-9336-26056c969195">GetThreadGroupSize</a>
</td>
<td align="left" width="63%">
Retrieves the sizes, in units of threads, of the X, Y, and Z dimensions of the shader's thread-group grid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c21756f-40f0-4459-852b-445053aa03e8">GetVariableByName</a>
</td>
<td align="left" width="63%">
Gets a variable by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e57cdb67-90b6-4d5d-967b-5de3a9bbaf78">IsSampleFrequencyShader</a>
</td>
<td align="left" width="63%">
Indicates whether a shader is a sample frequency shader.

</td>
</tr>
</table> 


## -remarks



An <b>ID3D11ShaderReflection</b> interface can be retrieved for a shader by using  <a href="https://msdn.microsoft.com/en-us/library/Dd607334(v=VS.85).aspx">D3DReflect</a>.  The following code illustrates retrieving a <b>ID3D11ShaderReflection</b>  from a shader.
          


```
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3DReflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            IID_ID3D11ShaderReflection, (void**) &pReflector);
```





## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

