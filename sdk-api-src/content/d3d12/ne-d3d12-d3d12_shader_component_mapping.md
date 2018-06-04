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

# D3D12_SHADER_COMPONENT_MAPPING enumeration


## -description



          Specifies how memory gets routed by a shader resource view (SRV).
        


## -enum-fields




### -field D3D12_SHADER_COMPONENT_MAPPING_FROM_MEMORY_COMPONENT_0


            Indicates return component 0 (red).
          


### -field D3D12_SHADER_COMPONENT_MAPPING_FROM_MEMORY_COMPONENT_1


            Indicates return component 1 (green).
          


### -field D3D12_SHADER_COMPONENT_MAPPING_FROM_MEMORY_COMPONENT_2


            Indicates return component 2 (blue).
          


### -field D3D12_SHADER_COMPONENT_MAPPING_FROM_MEMORY_COMPONENT_3


            Indicates return component 3 (alpha).
          


### -field D3D12_SHADER_COMPONENT_MAPPING_FORCE_VALUE_0


            Indicates forcing the resulting value to 0.
          


### -field D3D12_SHADER_COMPONENT_MAPPING_FORCE_VALUE_1


            Indicates forcing the resulting value 1.
            The value of forcing 1 is either 0x1 or 1.0f depending on the format type for that component in the source format.
          


## -remarks




          This enum allows the SRV to select how memory gets routed to the four return components in a shader after a memory fetch.  
          The options for each shader component [0..3] (corresponding to RGBA) are: component 0..3 from the SRV fetch result or force 0 or force 1.
        


          The default 1:1 mapping can be indicated by specifying D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING, 
          otherwise an arbitrary mapping can be specified using the macro D3D12_ENCODE_SHADER_4_COMPONENT_MAPPING.  
          See below.
        

Note the following defines:

<pre class="syntax" xml:space="preserve"><code>#define D3D12_SHADER_COMPONENT_MAPPING_MASK 0x7
#define D3D12_SHADER_COMPONENT_MAPPING_SHIFT 3
#define D3D12_SHADER_COMPONENT_MAPPING_ALWAYS_SET_BIT_AVOIDING_ZEROMEM_MISTAKES (1&lt;&lt;(D3D12_SHADER_COMPONENT_MAPPING_SHIFT*4))
#define D3D12_ENCODE_SHADER_4_COMPONENT_MAPPING(Src0,Src1,Src2,Src3) ((((Src0)&amp;D3D12_SHADER_COMPONENT_MAPPING_MASK)| \                                                                (((Src1)&amp;D3D12_SHADER_COMPONENT_MAPPING_MASK)&lt;&lt;D3D12_SHADER_COMPONENT_MAPPING_SHIFT)| \                                                               (((Src2)&amp;D3D12_SHADER_COMPONENT_MAPPING_MASK)&lt;&lt;(D3D12_SHADER_COMPONENT_MAPPING_SHIFT*2))| \                                                                (((Src3)&amp;D3D12_SHADER_COMPONENT_MAPPING_MASK)&lt;&lt;(D3D12_SHADER_COMPONENT_MAPPING_SHIFT*3))| \                                                                D3D12_SHADER_COMPONENT_MAPPING_ALWAYS_SET_BIT_AVOIDING_ZEROMEM_MISTAKES))
#define D3D12_DECODE_SHADER_4_COMPONENT_MAPPING(ComponentToExtract,Mapping) ((D3D12_SHADER_COMPONENT_MAPPING)(Mapping &gt;&gt; (D3D12_SHADER_COMPONENT_MAPPING_SHIFT*ComponentToExtract) &amp; D3D12_SHADER_COMPONENT_MAPPING_MASK))
#define D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING D3D12_ENCODE_SHADER_4_COMPONENT_MAPPING(0,1,2,3)
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

