---
UID: NN:d3d12shader.ID3D12ShaderReflectionVariable
title: ID3D12ShaderReflectionVariable
author: windows-sdk-content
description: This shader-reflection interface provides access to a variable.
old-location: direct3d12\id3d12shaderreflectionvariable.htm
tech.root: direct3d12
ms.assetid: E4CF0C77-2792-46DC-B38F-22C0ACBFD615
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D12ShaderReflectionVariable, ID3D12ShaderReflectionVariable interface, ID3D12ShaderReflectionVariable interface,described, d3d12shader/ID3D12ShaderReflectionVariable, direct3d12.id3d12shaderreflectionvariable
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
 - ID3D12ShaderReflectionVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12ShaderReflectionVariable interface


## -description


This shader-reflection interface provides access to a variable.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12ShaderReflectionVariable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12ShaderReflectionVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12ShaderReflectionVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/433FABE2-D0BB-4E97-84BB-D20566D32571">GetBuffer</a>
</td>
<td align="left" width="63%">
Returns the <a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer</a> of the present <b>ID3D12ShaderReflectionVariable</b>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21CF98AF-5645-4059-992A-FFF778576C93">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a shader-variable description.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6CD169C7-0C6B-4EC8-BF57-96EE5065CC9D">GetInterfaceSlot</a>
</td>
<td align="left" width="63%">
Gets the corresponding interface slot for a variable that represents an interface pointer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DE2BBC9F-3519-4896-96E1-40C2E726D8A1">GetType</a>
</td>
<td align="left" width="63%">
Gets a shader-variable type.
        

</td>
</tr>
</table> 


## -remarks



To get a shader-reflection-variable interface, call a method like <a href="https://msdn.microsoft.com/E79DACF1-2C89-42BB-BB04-DFA8280987C7">ID3D12ShaderReflection::GetVariableByName</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
          




## -see-also




<a href="https://msdn.microsoft.com/791d2c91-3791-47fe-b887-8117ecc798ba">Shader Interfaces</a>
 

 

