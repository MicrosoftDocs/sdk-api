---
UID: NS:d3d12.D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER
title: D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER
author: windows-sdk-content
description: Opaque data structure describing driver versioning for a serialized acceleration structure.
old-location: direct3d12\d3d12_serialized_data_driver_matching_identifier.htm
tech.root: direct3d12
ms.assetid: B98D2222-6ADC-4CA4-A75D-21162D7AB3F7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER, D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER structure, PD3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER, PD3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER structure pointer, d3d12/D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER, d3d12/PD3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER, direct3d12.d3d12_serialized_data_driver_matching_identifier
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER
product: Windows
targetos: Windows
req.typenames: D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER
req.redist: 
---

# D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Opaque data structure describing driver versioning for a serialized acceleration structure.  Pass this structure into a call to <a href="direct3d12.id3d12device5_checkdrivermatchingidentifier">ID3D12Device5::CheckDriverMatchingIdentifier</a> to determine if a previously serialized acceleration structure is compatible with the current driver/device, and can therefore be deserialized and used for raytracing.


## -struct-fields




### -field DriverOpaqueGUID

The opaque identifier of the driver.


### -field DriverOpaqueVersioningData

The opaque driver versioning data.

