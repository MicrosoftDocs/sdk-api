---
UID: NS:d3d12.D3D12_SHADER_RESOURCE_VIEW_DESC
title: D3D12_SHADER_RESOURCE_VIEW_DESC
author: windows-sdk-content
description: Describes a shader-resource view.
old-location: direct3d12\d3d12_shader_resource_view_desc.htm
old-project: direct3d12
ms.assetid: 2B4B868F-3E9F-4570-B1C7-2767ED717A3B
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: D3D12_SHADER_RESOURCE_VIEW_DESC, D3D12_SHADER_RESOURCE_VIEW_DESC structure, d3d12/D3D12_SHADER_RESOURCE_VIEW_DESC, direct3d12.d3d12_shader_resource_view_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: D3D12_SHADER_RESOURCE_VIEW_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_SHADER_RESOURCE_VIEW_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_SHADER_RESOURCE_VIEW_DESC structure


## -description


Describes a shader-resource view.


## -struct-fields




### -field Format


            A <a href="https://msdn.microsoft.com/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed value that  specifies the viewing format. See remarks.
          


### -field ViewDimension


            A <a href="https://msdn.microsoft.com/1834E70A-4193-4D75-AE47-5C423EACC349">D3D12_SRV_DIMENSION</a>-typed value that  specifies the resource type of the view. 
            This type is the same as the resource type of the underlying resource. 
            This member also determines which _SRV to use in the union below.
          


### -field Shader4ComponentMapping


            A <a href="https://msdn.microsoft.com/654E43DA-03C3-4BFB-8575-0BB48CB4FB81">D3D12_SHADER_COMPONENT_MAPPING</a> enumeration constant, such as return component 0 (red) from memory, or force the resulting value to 0.
            This mapping enables the shader resource view (SRV) to choose how memory gets routed to the 4 return components in a shader after a memory fetch.  
          


### -field Buffer


              A <a href="https://msdn.microsoft.com/FD5FBA65-4C70-487F-8D93-0EC5668BCE4A">D3D12_BUFFER_SRV</a> structure that views the resource as a buffer.
            


### -field Texture1D


              A <a href="https://msdn.microsoft.com/552DC1C1-8FFB-4BFC-8781-78B287CB70BD">D3D12_TEX1D_SRV</a> structure that views the resource as a 1D texture.
            


### -field Texture1DArray


              A <a href="https://msdn.microsoft.com/12931858-3E3C-4D4E-9459-7C15A73A485B">D3D12_TEX1D_ARRAY_SRV</a> structure that views the resource as a 1D-texture array.
            


### -field Texture2D


              A <a href="https://msdn.microsoft.com/BBD60A25-99C7-4C11-87F0-9E1D678EC44E">D3D12_TEX2D_SRV</a> structure that views the resource as a 2D-texture.
            


### -field Texture2DArray


              A <a href="https://msdn.microsoft.com/D3854008-0BB8-4284-A89F-A13DB85BB911">D3D12_TEX2D_ARRAY_SRV</a> structure that views the resource as a 2D-texture array.
            


### -field Texture2DMS


              A <a href="https://msdn.microsoft.com/65D0AC4E-E9D3-4D99-835C-AD9ED7528A1A">D3D12_TEX2DMS_SRV</a> structure that views the resource as a 2D-multisampled texture.
            


### -field Texture2DMSArray


              A <a href="https://msdn.microsoft.com/2AA430ED-4CE8-4EBD-9541-6EE0FFBA3873">D3D12_TEX2DMS_ARRAY_SRV</a> structure that views the resource as a 2D-multisampled-texture array.
            


### -field Texture3D


              A <a href="https://msdn.microsoft.com/21133B2B-7E12-489A-9AD6-4ACB6E6BAABC">D3D12_TEX3D_SRV</a> structure that views the resource as a 3D texture.
            


### -field TextureCube


              A <a href="https://msdn.microsoft.com/0924DE2B-73AE-473D-A35B-2DC8D8DBFC49">D3D12_TEXCUBE_SRV</a> structure that views the resource as a 3D-cube texture.
            


### -field TextureCubeArray


              A <a href="https://msdn.microsoft.com/58DDCEB5-A0B7-4E8D-ABE2-3B5B02C92D8D">D3D12_TEXCUBE_ARRAY_SRV</a> structure that views the resource as a 3D-cube-texture array.
            


## -remarks




          A view is a format-specific way to look at the data in a resource. The view determines what data to look at, and how it is cast when read.
        


          When viewing a resource, the resource-view description must specify a typed format, that is compatible with the resource format. So that means that you can't create a resource-view description using any format with _TYPELESS in the name. You can however view a typeless resource by specifying a typed format for the view. For example, a DXGI_FORMAT_R32G32B32_TYPELESS resource can be viewed with one of these typed formats: DXGI_FORMAT_R32G32B32_FLOAT, DXGI_FORMAT_R32G32B32_UINT, and DXGI_FORMAT_R32G32B32_SINT, since these typed formats are compatible with the typeless resource.
        


          Create a shader-resource-view description by calling <a href="https://msdn.microsoft.com/4FD7082D-2DA9-469E-BA74-6735D407D5FE">ID3D12Device::CreateShaderResourceView</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

