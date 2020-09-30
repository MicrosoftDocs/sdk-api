---
UID: NS:d3d12.D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER
title: D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER (d3d12.h)
description: Opaque data structure describing driver versioning for a serialized acceleration structure.
helpviewer_keywords: ["D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER","D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER structure","PD3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER","PD3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER structure pointer","d3d12/D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER","d3d12/PD3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER","direct3d12.d3d12_serialized_data_driver_matching_identifier"]
old-location: direct3d12\d3d12_serialized_data_driver_matching_identifier.htm
tech.root: direct3d12
ms.assetid: B98D2222-6ADC-4CA4-A75D-21162D7AB3F7
ms.date: 12/05/2018
ms.keywords: D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER, D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER structure, PD3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER, PD3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER structure pointer, d3d12/D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER, d3d12/PD3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER, direct3d12.d3d12_serialized_data_driver_matching_identifier
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
targetos: Windows
req.typenames: D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER
 - d3d12/D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER
---

# D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER structure


## -description

Opaque data structure describing driver versioning for a serialized acceleration structure.  Pass this structure into a call to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-checkdrivermatchingidentifier">ID3D12Device5::CheckDriverMatchingIdentifier</a> to determine if a previously serialized acceleration structure is compatible with the current driver/device, and can therefore be deserialized and used for raytracing.

## -struct-fields

### -field DriverOpaqueGUID

The opaque identifier of the driver.

### -field DriverOpaqueVersioningData

The opaque driver versioning data.