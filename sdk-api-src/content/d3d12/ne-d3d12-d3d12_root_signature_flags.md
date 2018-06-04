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

# D3D12_ROOT_SIGNATURE_FLAGS enumeration


## -description



          Specifies options for root signature layout.
        


## -enum-fields




### -field D3D12_ROOT_SIGNATURE_FLAG_NONE


            Indicates default behavior.
          


### -field D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT


            The app is opting in to using the Input Assembler (requiring an input layout that defines a set of vertex buffer bindings). Omitting this flag can result in one root argument space being saved on some hardware. Omit this flag if the Input Assembler is not required, though the optimization is minor.  


### -field D3D12_ROOT_SIGNATURE_FLAG_DENY_VERTEX_SHADER_ROOT_ACCESS


            Denies the vertex shader access to the root signature.
          


### -field D3D12_ROOT_SIGNATURE_FLAG_DENY_HULL_SHADER_ROOT_ACCESS


            Denies the hull shader access to the root signature.
          


### -field D3D12_ROOT_SIGNATURE_FLAG_DENY_DOMAIN_SHADER_ROOT_ACCESS


            Denies the domain shader access to the root signature.
          


### -field D3D12_ROOT_SIGNATURE_FLAG_DENY_GEOMETRY_SHADER_ROOT_ACCESS


            Denies the geometry shader access to the root signature.
          


### -field D3D12_ROOT_SIGNATURE_FLAG_DENY_PIXEL_SHADER_ROOT_ACCESS


            Denies the pixel shader access to the root signature.
          


### -field D3D12_ROOT_SIGNATURE_FLAG_ALLOW_STREAM_OUTPUT


            The root signature allows stream output.
            This flag can be specified for root signatures authored in HLSL, similar to how the other flags are specified.
            <a href="https://msdn.microsoft.com/E35FCC4A-7527-4A6C-8569-0801A06AA427">ID3D12Device::CreateGraphicsPipelineState</a> will fail if the geometry shader contains stream output but the root signature does not have this flag set.
          Omit this flag if stream output is not required.


## -remarks




        This enum is used in the <a href="https://msdn.microsoft.com/D74D9D3B-96AB-489A-A91C-4F68AC3D05EE">D3D12_ROOT_SIGNATURE_DESC</a> structure.
      

The value in denying access to shader stages is a minor optimization on some hardware. If, for example, the <a href="https://msdn.microsoft.com/1D66344A-110E-4190-BC00-9F88F1A3F8FB">D3D12_SHADER_VISIBILITY_ALL</a> flag has been set to broadcast the root signature to all shader stages, then denying access can overrule this and save the hardware some work. Alternatively if the shader is so simple that no root signature resources are needed, then denying access could be used here too.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/565B28C1-DBD1-42B6-87F9-70743E4A2E4A">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/D74D9D3B-96AB-489A-A91C-4F68AC3D05EE">D3D12_ROOT_SIGNATURE_DESC</a>
 

 

