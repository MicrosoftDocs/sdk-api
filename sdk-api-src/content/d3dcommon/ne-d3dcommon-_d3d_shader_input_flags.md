---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _D3D_SHADER_INPUT_FLAGS enumeration


## -description


Values that identify shader-input options.


## -enum-fields




### -field D3D_SIF_USERPACKED


            Assign a shader input to a register based on the register assignment in the HLSL code (instead of letting the compiler choose the register).
          


### -field D3D_SIF_COMPARISON_SAMPLER


            Use a comparison sampler, which uses the <a href="https://msdn.microsoft.com/e21894c4-e8c5-4c3d-92c1-727964f8fd94">SampleCmp (DirectX HLSL Texture Object)</a> and <a href="https://msdn.microsoft.com/cecfc5e8-d293-4e0e-a3f4-b23f84843b7d">SampleCmpLevelZero (DirectX HLSL Texture Object)</a> sampling functions.
          


### -field D3D_SIF_TEXTURE_COMPONENT_0


            A 2-bit value for encoding texture components.
          


### -field D3D_SIF_TEXTURE_COMPONENT_1


            A 2-bit value for encoding texture components.
          


### -field D3D_SIF_TEXTURE_COMPONENTS


            A 2-bit value for encoding texture components.
          


### -field D3D_SIF_UNUSED


            This value is reserved.
          


### -field D3D10_SIF_USERPACKED


            Assign a shader input to a register based on the register assignment in the HLSL code (instead of letting the compiler choose the register).
          


### -field D3D10_SIF_COMPARISON_SAMPLER


            Use a comparison sampler, which uses the <a href="https://msdn.microsoft.com/e21894c4-e8c5-4c3d-92c1-727964f8fd94">SampleCmp (DirectX HLSL Texture Object)</a> and <a href="https://msdn.microsoft.com/cecfc5e8-d293-4e0e-a3f4-b23f84843b7d">SampleCmpLevelZero (DirectX HLSL Texture Object)</a> sampling functions.
          


### -field D3D10_SIF_TEXTURE_COMPONENT_0


            A 2-bit value for encoding texture components.
          


### -field D3D10_SIF_TEXTURE_COMPONENT_1


            A 2-bit value for encoding texture components.
          


### -field D3D10_SIF_TEXTURE_COMPONENTS


            A 2-bit value for encoding texture components.
          


### -field D3D_SIF_FORCE_DWORD


            Forces the enumeration to compile to 32 bits.
            This value is not used directly by titles.
          


## -remarks



<b>D3D_SHADER_INPUT_FLAGS</b>-typed values are specified in
          the <b>uFlags</b> member of the <a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a> structure.
        




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

