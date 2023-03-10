---
UID: NS:directml.DML_FEATURE_QUERY_FEATURE_LEVELS
title: DML_FEATURE_QUERY_FEATURE_LEVELS
description: Used to query a DirectML device for its support for one or more feature levels.
tech.root: directml
ms.date: 10/30/2020
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: 
req.redist: 
f1_keywords:
 - DML_FEATURE_QUERY_FEATURE_LEVELS
 - directml/DML_FEATURE_QUERY_FEATURE_LEVELS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_FEATURE_QUERY_FEATURE_LEVELS
---

## -description

Used to query a DirectML device for its support for one or more feature levels. See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport). The feature constant is **DML_FEATURE_FEATURE_LEVELS**, and the support data type is [DML_FEATURE_DATA_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_data_feature_levels).

## -struct-fields

### -field RequestedFeatureLevelCount

Type: **[UINT](/windows/desktop/WinProg/windows-data-types)**

The number of elements in the *RequestedFeatureLevels* array.

### -field RequestedFeatureLevels

Type: \_Field\_size\_(RequestedFeatureLevelCount) **[DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)\***

An array of feature levels to query support for. When [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) returns, the [DML_FEATURE_DATA_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_data_feature_levels) struct contains the highest feature level in this array that is supported by the device.

## -remarks
This query is useful in combination with the *minimumFeatureLevel* parameter of [DMLCreateDevice1](/windows/win32/api/directml/nf-directml-dmlcreatedevice1). By supplying a minimum feature level to **DMLCreateDevice1**, you can be guaranteed a *lower* bound to the underlying DirectML device's feature level support.

Using this query, you can then also retrieve an *upper* bound for the feature levels supported by this DirectML device. This information can then be used to achieve graceful fallbacks in cases where particular features are unavailable.

## Availability
This API was introduced in DirectML version `1.1.0`.

## -see-also

[IDMLDevice::CheckFeatureSupport method](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)

[DML_FEATURE enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)

[DML_FEATURE_DATA_FEATURE_LEVELS structure](/windows/win32/api/directml/ns-directml-dml_feature_data_feature_levels)
