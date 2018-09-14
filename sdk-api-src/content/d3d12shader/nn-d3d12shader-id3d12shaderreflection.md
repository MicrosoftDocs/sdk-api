---
UID: NN:d3d12shader.ID3D12ShaderReflection
title: ID3D12ShaderReflection
author: windows-sdk-content
description: A shader-reflection interface accesses shader information.
old-location: direct3d12\id3d12shaderreflection.htm
tech.root: direct3d12
ms.assetid: 145F2CCB-C076-42BE-8AF4-74349CDF6B02
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ID3D12ShaderReflection, ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,described, d3d12shader/ID3D12ShaderReflection, direct3d12.id3d12shaderreflection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12ShaderReflection interface


## -description


A shader-reflection interface accesses shader information.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12ShaderReflection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12ShaderReflection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6862DC01-E75B-4913-882C-27C1CC659086">GetBitwiseInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of bitwise instructions.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84E3240C-D21F-4F71-9AC2-C89570571A72">GetConstantBufferByIndex</a>
</td>
<td align="left" width="63%">
Gets a constant buffer by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C8BE8C17-2B5A-45AB-8C39-778FFFA78992">GetConstantBufferByName</a>
</td>
<td align="left" width="63%">
Gets a constant buffer by name.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4425F608-4AFD-4065-AC8C-2EE4618D334B">GetConversionInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of conversion instructions.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D84DC99E-4E0C-4CFC-B061-FCD3C42D7937">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a shader description.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7A0E34F5-D2CF-41C2-B2CB-C3D0CDA511B3">GetGSInputPrimitive</a>
</td>
<td align="left" width="63%">
Gets the geometry-shader input-primitive description.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD1AFABD-E830-4292-96F4-278BA84E5B54">GetInputParameterDesc</a>
</td>
<td align="left" width="63%">
Gets an input-parameter description for a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DE1FC45B-DA2B-41B6-A732-62BA886F51C2">GetMinFeatureLevel</a>
</td>
<td align="left" width="63%">
Gets the minimum feature level.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9F002B65-F101-4498-A9C0-C545BCDB8CC1">GetMovcInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Movc instructions.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D8E6FFEE-2384-4B22-A12A-9527C4EEE26B">GetMovInstructionCount</a>
</td>
<td align="left" width="63%">
Gets the number of Mov instructions.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9D81990B-D5C3-495F-A0AC-E43712481093">GetNumInterfaceSlots</a>
</td>
<td align="left" width="63%">
Gets the number of interface slots in a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6B767F3A-54A7-40F0-B9A9-FD69FA07C689">GetOutputParameterDesc</a>
</td>
<td align="left" width="63%">
Gets an output-parameter description for a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01353250-0C8F-4C72-93CE-64BEF52EB985">GetPatchConstantParameterDesc</a>
</td>
<td align="left" width="63%">
Gets a patch-constant parameter description for a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ABA7BB9E-AB1D-407A-BB16-97EE74318C1A">GetRequiresFlags</a>
</td>
<td align="left" width="63%">
Gets a group of flags that indicates the requirements of a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3E9A168D-CD9E-4256-9E0B-19B9295E511E">GetResourceBindingDesc</a>
</td>
<td align="left" width="63%">
Gets a description of how a resource is bound to a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AA0FD49A-C5A2-4734-BDD6-FD739E4F5D59">GetResourceBindingDescByName</a>
</td>
<td align="left" width="63%">
Gets a description of how a resource is bound to a shader.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C34A76B7-2410-4F0D-B2EC-8C62CD70DFE0">GetThreadGroupSize</a>
</td>
<td align="left" width="63%">
Retrieves the sizes, in units of threads, of the X, Y, and Z dimensions of the shader's thread-group grid.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E79DACF1-2C89-42BB-BB04-DFA8280987C7">GetVariableByName</a>
</td>
<td align="left" width="63%">
Gets a variable by name.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8779992E-D20A-4D8A-82F2-B83A3D481BD9">IsSampleFrequencyShader</a>
</td>
<td align="left" width="63%">
Indicates whether a shader is a sample frequency shader.
        

</td>
</tr>
</table> 


## -remarks



An <b>ID3D12ShaderReflection</b> interface can be retrieved for a shader by using 
				<a href="https://msdn.microsoft.com/601cc907-2878-4c9b-bc48-0575fd4479e8">D3DReflect</a>.  
          




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/791d2c91-3791-47fe-b887-8117ecc798ba">Shader Interfaces</a>
 

 

