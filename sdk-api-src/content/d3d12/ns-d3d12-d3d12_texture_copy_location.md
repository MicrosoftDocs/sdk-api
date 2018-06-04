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

# D3D12_TEXTURE_COPY_LOCATION structure


## -description


Describes a portion of a texture for the purpose of texture copies. 


## -struct-fields




### -field pResource


            Specifies the resource which will be used for the copy operation.<div> </div>
            When <b>Type</b> is D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT, <b>pResource</b> must point to a buffer resource.<div> </div>
            When <b>Type</b> is D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX, <b>pResource</b> must point to a texture resource.
          


### -field Type


            Specifies which type of resource location this is: a subresource of a texture, or a description of a texture layout which can be applied to a buffer.
            This <a href="https://msdn.microsoft.com/CF296200-55A7-46B2-BF2C-58806A6A3BBC">D3D12_TEXTURE_COPY_TYPE</a> enum indicates which union member to use.
          


### -field PlacedFootprint


              Specifies a texture layout, with offset, dimensions, and pitches, for the hardware to understand how to treat a section of a buffer resource as a multi-dimensional texture.
              To fill-in the correct data for a <a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">CopyTextureRegion</a> call, 
              see <a href="https://msdn.microsoft.com/74740A52-C2A5-4AF6-92CC-85B5C214423F">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a>.
            


### -field SubresourceIndex


              Specifies the index of the subresource of an arrayed, mip-mapped, or planar texture should be used for the copy operation.
            


## -remarks




          Use this structure with <a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">CopyTextureRegion</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/8BA93729-2FFB-4C09-88B0-779049BAF385">CD3DX12_TEXTURE_COPY_LOCATION</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/74740A52-C2A5-4AF6-92CC-85B5C214423F">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a>
 

 

