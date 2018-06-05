---
UID: NS:d3d12.D3D12_TEXTURE_COPY_LOCATION
title: D3D12_TEXTURE_COPY_LOCATION
author: windows-sdk-content
description: Describes a portion of a texture for the purpose of texture copies.
old-location: direct3d12\d3d12_texture_copy_location.htm
old-project: direct3d12
ms.assetid: D63EC731-EE75-44CD-9CCD-7FB4A761D1A3
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_TEXTURE_COPY_LOCATION, D3D12_TEXTURE_COPY_LOCATION structure, d3d12/D3D12_TEXTURE_COPY_LOCATION, direct3d12.d3d12_texture_copy_location
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
req.typenames: D3D12_TEXTURE_COPY_LOCATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_TEXTURE_COPY_LOCATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

