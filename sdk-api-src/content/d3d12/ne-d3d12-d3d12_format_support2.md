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

# D3D12_FORMAT_SUPPORT2 enumeration


## -description



          Specifies which unordered resource options are supported for a provided format.
        


## -enum-fields




### -field D3D12_FORMAT_SUPPORT2_NONE

No unordered resource options are supported.


### -field D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD

Format supports atomic add.


### -field D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS

Format supports atomic bitwise operations.


### -field D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE

Format supports atomic compare with store or exchange.


### -field D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE

Format supports atomic exchange.


### -field D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX

Format supports atomic min and max.


### -field D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX

Format supports atomic unsigned min and max.


### -field D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD

Format supports a typed load.


### -field D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE

Format supports a typed store.


### -field D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP

Format supports logic operations in blend state.


### -field D3D12_FORMAT_SUPPORT2_TILED


              Format supports tiled resources. Refer to <a href="https://msdn.microsoft.com/F670D15D-BC0F-4F90-99C1-A35192FE8980">Volume Tiled Resources</a>.
            


### -field D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY


            Format supports multi-plane overlays.
          


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/6E4EB08F-0B60-4B1E-AD27-8F0AE2BD0766">D3D12_FEATURE_DATA_FORMAT_SUPPORT</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

