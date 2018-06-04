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

# D3D12_STATIC_SAMPLER_DESC structure


## -description



          Describes a static sampler.
        


## -struct-fields




### -field Filter


            The filtering method to use when sampling a texture, as a <a href="https://msdn.microsoft.com/3755A722-34E5-415E-8760-93094D033E05">D3D12_FILTER</a> enumeration constant.
          


### -field AddressU


             Specifies the <a href="https://msdn.microsoft.com/7F67C8B6-1B01-49C0-9900-AFDBEDE5508F">D3D12_TEXTURE_ADDRESS_MODE</a> mode to use for resolving a <i>u</i> texture coordinate that is outside the 0 to 1 range.
         


### -field AddressV


            Specifies the <a href="https://msdn.microsoft.com/7F67C8B6-1B01-49C0-9900-AFDBEDE5508F">D3D12_TEXTURE_ADDRESS_MODE</a> mode to use for resolving a <i>v</i> texture coordinate that is outside the 0 to 1 range.
          


### -field AddressW


            Specifies the <a href="https://msdn.microsoft.com/7F67C8B6-1B01-49C0-9900-AFDBEDE5508F">D3D12_TEXTURE_ADDRESS_MODE</a> mode to use for resolving a <i>w</i> texture coordinate that is outside the 0 to 1 range.
          


### -field MipLODBias


            Offset from the calculated mipmap level. For example, if Direct3D calculates that a texture should be sampled at mipmap level 3 and MipLODBias is 2, then the texture will be sampled at mipmap level 5.
          


### -field MaxAnisotropy


            Clamping value used if D3D12_FILTER_ANISOTROPIC or D3D12_FILTER_COMPARISON_ANISOTROPIC is specified as the filter. Valid values are between 1 and 16.
          


### -field ComparisonFunc


            A function that compares sampled data against existing sampled data. 
            The function options are listed in <a href="https://msdn.microsoft.com/68223746-59B3-4FDD-B7EF-44557F1C46E3">D3D12_COMPARISON_FUNC</a>.
          


### -field BorderColor


            One member of <a href="https://msdn.microsoft.com/E5D3E447-F1C7-4AAF-B9AB-829C33622E34">D3D12_STATIC_BORDER_COLOR</a>, the border color to use if D3D12_TEXTURE_ADDRESS_MODE_BORDER is specified for AddressU, AddressV, or AddressW. 
            Range must be between 0.0 and 1.0 inclusive.
          


### -field MinLOD


            Lower end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed.
          


### -field MaxLOD


            Upper end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed. This value must be greater than or equal to MinLOD. To have no upper limit on LOD set this to a large value such as D3D12_FLOAT32_MAX.
          


### -field ShaderRegister


              The <i>ShaderRegister</i> and <i>RegisterSpace</i> parameters correspond to the binding syntax of HLSL.  For example, in HLSL:
            

<pre class="syntax" xml:space="preserve"><code>Texture2D&lt;float4&gt; a : register(t2, space3);</code></pre>

              This corresponds to a  <i>ShaderRegister</i> of 2 (indicating the type is SRV), and <i>RegisterSpace</i> is 3.
            


              The  <i>ShaderRegister</i> and <i>RegisterSpace</i> pair is needed to establish correspondence between shader resources and runtime heap descriptors, using the root signature data structure.
            


### -field RegisterSpace


            See the description for <i>ShaderRegister</i>.
            Register space is optional; the default register space is 0.
          


### -field ShaderVisibility


            Specifies the visibility of the sampler to the pipeline shaders, one member of <a href="https://msdn.microsoft.com/1D66344A-110E-4190-BC00-9F88F1A3F8FB">D3D12_SHADER_VISIBILITY</a>.
          


## -remarks




        Use this structure with the <a href="https://msdn.microsoft.com/D74D9D3B-96AB-489A-A91C-4F68AC3D05EE">D3D12_ROOT_SIGNATURE_DESC</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/C402415D-7BD5-4E23-82C9-B29B0B5669B8">CD3DX12_STATIC_SAMPLER_DESC</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

