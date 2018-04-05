---
UID: NE:d3d12.D3D12_FORMAT_SUPPORT2
title: D3D12_FORMAT_SUPPORT2
author: windows-driver-content
description: Specifies which unordered resource options are supported for a provided format.
old-location: direct3d12\d3d12_format_support2.htm
old-project: direct3d12
ms.assetid: 29B53FBE-2FF3-4A3A-8392-30781541C396
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D12_FORMAT_SUPPORT2, D3D12_FORMAT_SUPPORT2 enumeration, D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY, D3D12_FORMAT_SUPPORT2_NONE, D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP, D3D12_FORMAT_SUPPORT2_TILED, D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD, D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS, D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE, D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE, D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX, D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX, D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD, D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE, d3d12/D3D12_FORMAT_SUPPORT2, d3d12/D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY, d3d12/D3D12_FORMAT_SUPPORT2_NONE, d3d12/D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP, d3d12/D3D12_FORMAT_SUPPORT2_TILED, d3d12/D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD, d3d12/D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS, d3d12/D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE, d3d12/D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE, d3d12/D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX, d3d12/D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX, d3d12/D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD, d3d12/D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE, direct3d12.d3d12_format_support2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3D12_FORMAT_SUPPORT2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_FORMAT_SUPPORT2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

