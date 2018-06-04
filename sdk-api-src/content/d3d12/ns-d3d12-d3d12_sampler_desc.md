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

# D3D12_SAMPLER_DESC structure


## -description


Describes a sampler state.


## -struct-fields




### -field Filter


            A <a href="https://msdn.microsoft.com/3755A722-34E5-415E-8760-93094D033E05">D3D12_FILTER</a>-typed value that specifies the filtering method to use when sampling a texture.
          


### -field AddressU


            A <a href="https://msdn.microsoft.com/7F67C8B6-1B01-49C0-9900-AFDBEDE5508F">D3D12_TEXTURE_ADDRESS_MODE</a>-typed value that specifies the method to use for resolving a u texture coordinate that is outside the 0 to 1 range.
          


### -field AddressV


            A <a href="https://msdn.microsoft.com/7F67C8B6-1B01-49C0-9900-AFDBEDE5508F">D3D12_TEXTURE_ADDRESS_MODE</a>-typed value that specifies the method to use for resolving a v texture coordinate that is outside the 0 to 1 range.
          


### -field AddressW


            A <a href="https://msdn.microsoft.com/7F67C8B6-1B01-49C0-9900-AFDBEDE5508F">D3D12_TEXTURE_ADDRESS_MODE</a>-typed value that specifies the method to use for resolving a w texture coordinate that is outside the 0 to 1 range.
          


### -field MipLODBias


            Offset from the calculated mipmap level. For example, if the runtime calculates that a texture should be sampled at mipmap level 3 and <b>MipLODBias</b> is 2, the texture will be sampled at mipmap level 5.
          


### -field MaxAnisotropy


            Clamping value used if <b>D3D12_FILTER_ANISOTROPIC</b> or <b>D3D12_FILTER_COMPARISON_ANISOTROPIC</b> is specified in <b>Filter</b>. Valid values are between 1 and 16.
          


### -field ComparisonFunc


            A <a href="https://msdn.microsoft.com/68223746-59B3-4FDD-B7EF-44557F1C46E3">D3D12_COMPARISON_FUNC</a>-typed value that specifies a function that compares sampled data against existing sampled data.
          


### -field BorderColor


            Border color to use if <a href="d3d12_texture_address_mode.htm">D3D12_TEXTURE_ADDRESS_MODE_BORDER</a> is specified for <b>AddressU</b>, <b>AddressV</b>, or <b>AddressW</b>. Range must be between 0.0 and 1.0 inclusive.
          


### -field MinLOD

Lower end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed.


### -field MaxLOD


            Upper end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed. This value must be greater than or equal to <b>MinLOD</b>. To have no upper limit on LOD, set this member to a large value.
          


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/453B2D3D-843E-4DB0-BC47-59BD9C78BFD6">CreateSampler</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

