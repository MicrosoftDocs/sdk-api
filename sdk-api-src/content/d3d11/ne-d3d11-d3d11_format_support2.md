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

# D3D11_FORMAT_SUPPORT2 enumeration


## -description



      Unordered resource support options for a compute shader resource (see <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a>).


## -enum-fields




### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD

Format supports atomic add.


### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS

Format supports atomic bitwise operations.


### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE

Format supports atomic compare with store or exchange.


### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE

Format supports atomic exchange.


### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX

Format supports atomic min and max.


### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX

Format supports atomic unsigned min and max.


### -field D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD

Format supports a typed load.


### -field D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE

Format supports a typed store.


### -field D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP

Format supports logic operations in blend state.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


### -field D3D11_FORMAT_SUPPORT2_TILED

Format supports tiled resources.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.


### -field D3D11_FORMAT_SUPPORT2_SHAREABLE


              Format supports shareable resources.
              <div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R8G8B8A8_UNORM</a> and <b>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</b> are never shareable when using feature level 9, even if the device indicates optional feature support for <b>D3D11_FORMAT_SUPPORT_SHAREABLE</b>.
                Attempting to create shared resources with DXGI formats <b>DXGI_FORMAT_R8G8B8A8_UNORM</b> and <b>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</b> will always fail unless the feature level is 10_0 or higher.
              </div>
<div> </div>


<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.


### -field D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY

Format supports multi-plane overlays. 




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

