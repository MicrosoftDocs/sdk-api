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

# D3D11_FEATURE_DATA_D3D11_OPTIONS2 structure


## -description


Describes Direct3D 11.3 feature options in the current graphics driver.


## -struct-fields




### -field PSSpecifiedStencilRefSupported


            Specifies whether the hardware and driver support <b>PSSpecifiedStencilRef</b>.
            The runtime sets this member to <b>TRUE</b> if the hardware and driver support this option.
          


### -field TypedUAVLoadAdditionalFormats


            Specifies whether the hardware and driver support <b>TypedUAVLoadAdditionalFormats</b>.
            The runtime sets this member to <b>TRUE</b> if the hardware and driver support this option.
          


### -field ROVsSupported


            Specifies whether the hardware and driver support ROVs.
            The runtime sets this member to <b>TRUE</b> if the hardware and driver support this option.
          


### -field ConservativeRasterizationTier


            Specifies whether the hardware and driver support conservative rasterization.
            The runtime sets this member to a <a href="https://msdn.microsoft.com/1409ACE8-960C-4297-80D9-DAD3CD1886AD">D3D11_CONSERVATIVE_RASTERIZATION_TIER</a>-typed value that indicates if the hardware and driver support conservative rasterization and at what tier level.
          


### -field TiledResourcesTier


            Specifies whether the hardware and driver support tiled resources.
            The runtime sets this member to a <a href="https://msdn.microsoft.com/F2E58CDC-4E65-4166-976A-E58B6DC7B1E8">D3D11_TILED_RESOURCES_TIER</a>-typed value that indicates if the hardware and driver support tiled resources and at what tier level.
          


### -field MapOnDefaultTextures


            Specifies whether the hardware and driver support mapping on default textures.
            The runtime sets this member to <b>TRUE</b> if the hardware and driver support this option.
          


### -field StandardSwizzle


            Specifies whether the hardware and driver support standard swizzle.
            The runtime sets this member to <b>TRUE</b> if the hardware and driver support this option.
          


### -field UnifiedMemoryArchitecture


            Specifies whether the hardware and driver support Unified Memory Architecture.
            The runtime sets this member to <b>TRUE</b> if the hardware and driver support this option.
          


## -remarks




        If <b>MapOnDefaultTextures</b> is TRUE, applications may create textures using D3D11_USAGE_DEFAULT in combination with non-zero a D3D11_CPU_ACCESS_FLAG value.
        For performance reasons it is typically undesirable to create a default texture with CPU access flags unless the <b>UnifiedMemoryArchitecture</b> option is TRUE, or CPU / GPU usage of the texture is tightly interleaved.
      


        Default textures may not be in a mapped state while either bound to the pipeline to referenced by an operation issued to a context.
        Default textures may not be mapped by a deferred context.
        Default textures may not be created shareable.
      


        See <a href="https://msdn.microsoft.com/E7786550-99FC-4F8E-B93F-C2877C052EC2">D3D11_TEXTURE_LAYOUT</a> for texture swizzle options and restrictions.
      




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

