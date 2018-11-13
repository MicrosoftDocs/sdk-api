---
UID: NN:d3d12shader.ID3D12ShaderReflectionType
title: ID3D12ShaderReflectionType
author: windows-sdk-content
description: This shader-reflection interface provides access to variable type.
old-location: direct3d12\id3d12shaderreflectiontype.htm
tech.root: direct3d12
ms.assetid: 78FF30C5-7F23-489D-9E9D-916F6CE09C0E
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: ID3D12ShaderReflectionType, ID3D12ShaderReflectionType interface, ID3D12ShaderReflectionType interface,described, d3d12shader/ID3D12ShaderReflectionType, direct3d12.id3d12shaderreflectiontype
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
 - ID3D12ShaderReflectionType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12ShaderReflectionType interface


## -description


This shader-reflection interface provides access to variable type.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12ShaderReflectionType</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12ShaderReflectionType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12ShaderReflectionType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87EC1297-0951-4BE5-8CAC-BA71FB6237C0">GetBaseClass</a>
</td>
<td align="left" width="63%">
Gets an <b>ID3D12ShaderReflectionType Interface</b>  interface containing the variable base class type.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E5C28FFE-5BA4-436F-9CDB-215B5B9918F9">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the description of a shader-reflection-variable type.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1B9DABC6-65CA-47E3-95BF-77F29AC9D751">GetInterfaceByIndex</a>
</td>
<td align="left" width="63%">
Gets an interface by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59940F25-D394-4DA6-8493-B3B04C68B1CC">GetMemberTypeByIndex</a>
</td>
<td align="left" width="63%">
Gets a shader-reflection-variable type by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1A05A112-3975-4424-AED7-55F9CFBF8771">GetMemberTypeByName</a>
</td>
<td align="left" width="63%">
Gets a shader-reflection-variable type by name.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/113510A0-6F0D-4B30-8C6A-D0266570160E">GetMemberTypeName</a>
</td>
<td align="left" width="63%">
Gets a shader-reflection-variable type.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6BE5DACB-EDAB-4A95-A071-F36046858FFE">GetNumInterfaces</a>
</td>
<td align="left" width="63%">
Gets the number of interfaces.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FE91228D-F9DD-47F1-84E7-08D3C7E424C4">GetSubType</a>
</td>
<td align="left" width="63%">
Gets the base class of a class.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FE84D58A-998D-4362-96B2-5C00D2A82CB8">ImplementsInterface</a>
</td>
<td align="left" width="63%">
Indicates whether a class type implements an interface.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C1EAFAA2-6D35-4D4A-9153-98D927375EAD">IsEqual</a>
</td>
<td align="left" width="63%">
Indicates whether two <b>ID3D12ShaderReflectionType Interface</b> pointers have the same underlying type.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6B5A043A-927A-49AD-BF63-F8A9CCB57E09">IsOfType</a>
</td>
<td align="left" width="63%">
Indicates whether a variable is of the specified type.
        

</td>
</tr>
</table> 


## -remarks



The get a shader-reflection-type interface, call <a href="https://msdn.microsoft.com/DE2BBC9F-3519-4896-96E1-40C2E726D8A1">ID3D12ShaderReflectionVariable::GetType</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
          




## -see-also




<a href="https://msdn.microsoft.com/791d2c91-3791-47fe-b887-8117ecc798ba">Shader Interfaces</a>
 

 

