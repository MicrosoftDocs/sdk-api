---
UID: NE:d3d12.D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS
title: D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS (d3d12.h)
description: Specifies the result of a call to ID3D12Device5::CheckDriverMatchingIdentifier which queries whether serialized data is compatible with the current device and driver version.
helpviewer_keywords: ["D3D12_DRIVER_MATCHING_IDENTIFIER_COMPATIBLE_WITH_DEVICE","D3D12_DRIVER_MATCHING_IDENTIFIER_INCOMPATIBLE_TYPE","D3D12_DRIVER_MATCHING_IDENTIFIER_INCOMPATIBLE_VERSION","D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS","D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS enumeration","D3D12_DRIVER_MATCHING_IDENTIFIER_UNRECOGNIZED","D3D12_DRIVER_MATCHING_IDENTIFIER_UNSUPPORTED_TYPE","d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_COMPATIBLE_WITH_DEVICE","d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_INCOMPATIBLE_TYPE","d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_INCOMPATIBLE_VERSION","d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS","d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_UNRECOGNIZED","d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_UNSUPPORTED_TYPE","direct3d12.d3d12_driver_matching_identifier_status"]
old-location: direct3d12\d3d12_driver_matching_identifier_status.htm
tech.root: direct3d12
ms.assetid: 57FC8ECA-DA50-485F-8B1F-6AFE2D1BAA29
ms.date: 12/05/2018
ms.keywords: D3D12_DRIVER_MATCHING_IDENTIFIER_COMPATIBLE_WITH_DEVICE, D3D12_DRIVER_MATCHING_IDENTIFIER_INCOMPATIBLE_TYPE, D3D12_DRIVER_MATCHING_IDENTIFIER_INCOMPATIBLE_VERSION, D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS, D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS enumeration, D3D12_DRIVER_MATCHING_IDENTIFIER_UNRECOGNIZED, D3D12_DRIVER_MATCHING_IDENTIFIER_UNSUPPORTED_TYPE, d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_COMPATIBLE_WITH_DEVICE, d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_INCOMPATIBLE_TYPE, d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_INCOMPATIBLE_VERSION, d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS, d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_UNRECOGNIZED, d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_UNSUPPORTED_TYPE, direct3d12.d3d12_driver_matching_identifier_status
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
req.typenames: D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS
 - d3d12/D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS
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
 - D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS
---

# D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS enumeration


## -description

Specifies the result of a call to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-checkdrivermatchingidentifier">ID3D12Device5::CheckDriverMatchingIdentifier</a> which queries whether serialized data is compatible with the current device and driver version.

## -enum-fields

### -field D3D12_DRIVER_MATCHING_IDENTIFIER_COMPATIBLE_WITH_DEVICE:0

Serialized data is compatible with the current device/driver.

### -field D3D12_DRIVER_MATCHING_IDENTIFIER_UNSUPPORTED_TYPE:0x1

The specified <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_serialized_data_type">D3D12_SERIALIZED_DATA_TYPE</a> specified is unknown or unsupported.

### -field D3D12_DRIVER_MATCHING_IDENTIFIER_UNRECOGNIZED:0x2

Format of the data in <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_serialized_data_driver_matching_identifier">D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER</a> is unrecognized.  This could indicate either corrupt data or the identifier was produced by a different hardware vendor.

### -field D3D12_DRIVER_MATCHING_IDENTIFIER_INCOMPATIBLE_VERSION:0x3

Serialized data is recognized, but its version is not compatible with the current driver. This result may indicate that the device is from the same hardware vendor but is an incompatible version.

### -field D3D12_DRIVER_MATCHING_IDENTIFIER_INCOMPATIBLE_TYPE:0x4

<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_serialized_data_type">D3D12_SERIALIZED_DATA_TYPE</a> specifies a data type that is not compatible with the type of serialized data.  As long as there is only a single defined serialized data type this error cannot not be produced.
