---
UID: NE:d3d12.D3D12_ROOT_SIGNATURE_FLAGS
title: D3D12_ROOT_SIGNATURE_FLAGS
author: windows-sdk-content
description: Specifies options for root signature layout.
old-location: direct3d12\d3d12_root_signature_flags.htm
tech.root: direct3d12
ms.assetid: C3118E58-2006-459F-B2D6-4EC84F2BC058
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D12_ROOT_SIGNATURE_FLAGS, D3D12_ROOT_SIGNATURE_FLAGS enumeration, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_STREAM_OUTPUT, D3D12_ROOT_SIGNATURE_FLAG_DENY_DOMAIN_SHADER_ROOT_ACCESS, D3D12_ROOT_SIGNATURE_FLAG_DENY_GEOMETRY_SHADER_ROOT_ACCESS, D3D12_ROOT_SIGNATURE_FLAG_DENY_HULL_SHADER_ROOT_ACCESS, D3D12_ROOT_SIGNATURE_FLAG_DENY_PIXEL_SHADER_ROOT_ACCESS, D3D12_ROOT_SIGNATURE_FLAG_DENY_VERTEX_SHADER_ROOT_ACCESS, D3D12_ROOT_SIGNATURE_FLAG_LOCAL_ROOT_SIGNATURE, D3D12_ROOT_SIGNATURE_FLAG_NONE, d3d12/D3D12_ROOT_SIGNATURE_FLAGS, d3d12/D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT, d3d12/D3D12_ROOT_SIGNATURE_FLAG_ALLOW_STREAM_OUTPUT, d3d12/D3D12_ROOT_SIGNATURE_FLAG_DENY_DOMAIN_SHADER_ROOT_ACCESS, d3d12/D3D12_ROOT_SIGNATURE_FLAG_DENY_GEOMETRY_SHADER_ROOT_ACCESS, d3d12/D3D12_ROOT_SIGNATURE_FLAG_DENY_HULL_SHADER_ROOT_ACCESS, d3d12/D3D12_ROOT_SIGNATURE_FLAG_DENY_PIXEL_SHADER_ROOT_ACCESS, d3d12/D3D12_ROOT_SIGNATURE_FLAG_DENY_VERTEX_SHADER_ROOT_ACCESS, d3d12/D3D12_ROOT_SIGNATURE_FLAG_LOCAL_ROOT_SIGNATURE, d3d12/D3D12_ROOT_SIGNATURE_FLAG_NONE, direct3d12.d3d12_root_signature_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_ROOT_SIGNATURE_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_ROOT_SIGNATURE_FLAGS
req.redist: 
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

The root signature is to be used with raytracing shaders to define resource bindings sourced from shader records in shader tables.  This flag cannot be combined with any other root signature flags, which are all related to the graphics pipeline.  The absence of the flag means the root signature can be used with graphics or compute, where the compute version is also shared with raytracing’s global root signature.


### -field D3D12_ROOT_SIGNATURE_FLAG_LOCAL_ROOT_SIGNATURE

Denies the domain shader access to the root signature.
          


## -remarks



This enum is used in the <a href="https://msdn.microsoft.com/D74D9D3B-96AB-489A-A91C-4F68AC3D05EE">D3D12_ROOT_SIGNATURE_DESC</a> structure.
      

The value in denying access to shader stages is a minor optimization on some hardware. If, for example, the <a href="https://msdn.microsoft.com/1D66344A-110E-4190-BC00-9F88F1A3F8FB">D3D12_SHADER_VISIBILITY_ALL</a> flag has been set to broadcast the root signature to all shader stages, then denying access can overrule this and save the hardware some work. Alternatively if the shader is so simple that no root signature resources are needed, then denying access could be used here too.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/565B28C1-DBD1-42B6-87F9-70743E4A2E4A">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/D74D9D3B-96AB-489A-A91C-4F68AC3D05EE">D3D12_ROOT_SIGNATURE_DESC</a>
 

 

