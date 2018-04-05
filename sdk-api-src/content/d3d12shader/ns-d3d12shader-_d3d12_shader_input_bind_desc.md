---
UID: NS:d3d12shader._D3D12_SHADER_INPUT_BIND_DESC
title: "_D3D12_SHADER_INPUT_BIND_DESC"
author: windows-driver-content
description: Describes how a shader resource is bound to a shader input.
old-location: direct3d12\d3d12_shader_input_bind_desc.htm
old-project: direct3d12
ms.assetid: 4179C417-388D-4A20-8878-D074E20A706F
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D12_SHADER_INPUT_BIND_DESC, D3D12_SHADER_INPUT_BIND_DESC structure, _D3D12_SHADER_INPUT_BIND_DESC, d3d12shader/D3D12_SHADER_INPUT_BIND_DESC, direct3d12.d3d12_shader_input_bind_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: D3D12_SHADER_INPUT_BIND_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12shader.h
api_name:
-	D3D12_SHADER_INPUT_BIND_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D12_SHADER_INPUT_BIND_DESC structure


## -description



          Describes how a shader resource is bound to a shader input.
        


## -struct-fields




### -field Name


            Name of the shader resource.
          


### -field Type


            A <a href="https://msdn.microsoft.com/c6106f9e-420d-43e1-92ba-bc3a6e544e7d">D3D_SHADER_INPUT_TYPE</a>-typed value that identifies the type of data in the resource.
          


### -field BindPoint


            Starting bind point.
          


### -field BindCount


            Number of contiguous bind points for arrays.
          


### -field uFlags


            A combination of <a href="https://msdn.microsoft.com/3c79331e-73c0-42d7-9948-6ac2671a4ab5">D3D_SHADER_INPUT_FLAGS</a>-typed values for shader input-parameter options.
          


### -field ReturnType


            If the input is a texture, the <a href="https://msdn.microsoft.com/3da3f315-9f92-4557-93b8-94aff42a91fe">D3D_RESOURCE_RETURN_TYPE</a>-typed value that identifies the return type.
          


### -field Dimension


            A <a href="https://msdn.microsoft.com/6f3c2429-83be-44cd-89bb-b074bfa084e3">D3D_SRV_DIMENSION</a>-typed value that identifies the dimensions of the bound resource.
          


### -field NumSamples


            The number of samples for a multisampled texture; when a texture isn't multisampled, the value is set to -1 (0xFFFFFFFF).
            This is zero if the shader resource is not a recognized texture.
          


### -field Space


            The register space.
          


### -field uID


            The range ID in the bytecode.
          


## -remarks




        Get a shader-input-signature description by calling <a href="https://msdn.microsoft.com/3E9A168D-CD9E-4256-9E0B-19B9295E511E">ID3D12ShaderReflection::GetResourceBindingDesc</a> or <a href="https://msdn.microsoft.com/AA0FD49A-C5A2-4734-BDD6-FD739E4F5D59">ID3D12ShaderReflection::GetResourceBindingDescByName</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0">Shader Structures</a>
 

 

