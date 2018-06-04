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

# D3D11_TILED_RESOURCES_TIER enumeration


## -description


Indicates the tier level at which tiled resources are supported.


## -enum-fields




### -field D3D11_TILED_RESOURCES_NOT_SUPPORTED

Tiled resources are not supported.


### -field D3D11_TILED_RESOURCES_TIER_1


            Tier_1 tiled resources are supported.


              The device supports calls to <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">CreateTexture2D</a> and so on with the <a href="d3d11_resource_misc_flag.htm">D3D11_RESOURCE_MISC_TILED</a> flag.
            


              The device supports calls to <a href="https://msdn.microsoft.com/5aec93c5-12a1-4b4e-813e-ee1e85adbf14">CreateBuffer</a> with the <a href="d3d11_resource_misc_flag.htm">D3D11_RESOURCE_MISC_TILE_POOL</a> flag.
            


              If you access tiles (read or write) that are <b>NULL</b>-mapped, you get undefined behavior, which includes device-removed.  Apps can map all tiles to a single "default" tile to avoid this condition.
            


### -field D3D11_TILED_RESOURCES_TIER_2


            Tier_2 tiled resources are supported.
            


                Superset of Tier_1 functionality, which includes this additional support:
              

<ul>
<li>
                On Tier_1, if the size of a texture mipmap level is an integer multiple of the standard tile shape for its format, it is guaranteed to be nonpacked. On Tier_2, this guarantee is expanded to include mipmap levels whose size is at least one standard tile shape.
                For more info, see <a href="https://msdn.microsoft.com/1c200c44-6cd6-4e77-8187-54cd6cd79c84">D3D11_PACKED_MIP_DESC</a>.
              </li>
<li>
                Shader instructions are available for clamping level-of-detail (LOD) and for obtaining status about the shader operation. For info about one of these shader instructions, see <a href="https://msdn.microsoft.com/1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F">Sample(S,float,int,float,uint)</a>.
              </li>
<li>
                Reading from <b>NULL</b>-mapped tiles treat that sampled value as zero.  Writes to <b>NULL</b>-mapped tiles are discarded.
              </li>
</ul>

### -field D3D11_TILED_RESOURCES_TIER_3


            Tier_3 tiled resources are supported.
            


                Superset of Tier_2 functionality, Tier 3 is essentially Tier 2 but with the additional support of Texture3D for Tiled Resources.


## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>



<a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a>
 

 

