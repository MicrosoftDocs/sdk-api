---
UID: NS:directml.DML_FEATURE_DATA_FEATURE_LEVELS
title: DML_FEATURE_DATA_FEATURE_LEVELS
description: Provides detail about the feature levels supported by a DirectML device.
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
 - DML_FEATURE_DATA_FEATURE_LEVELS
 - directml/DML_FEATURE_DATA_FEATURE_LEVELS
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
 - DML_FEATURE_DATA_FEATURE_LEVELS
---

## -description

Provides detail about the feature levels supported by a DirectML device. See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport). The feature constant is **DML_FEATURE_FEATURE_LEVELS**, and the query data type is [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels).

## -struct-fields

### -field MaxSupportedFeatureLevel

Type: **[DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)**

The highest feature level supplied in the query structure's *RequestedFeatureLevels* (see [DML_FEATURE_DATA_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_data_feature_levels)) that is supported by this device.

> [!NOTE]
> Because this feature query only ever returns one of the values supplied in *RequestedFeatureLevels*, it's possible that the device supports an even higher feature level than the one returned by this query.

For example, DirectML version `1.4.0` supports a feature level of `DML_FEATURE_LEVEL_3_0`. If the *RequestedFeatureLevels* array contained only `DML_FEATURE_LEVEL_1_0` and `DML_FEATURE_LEVEL_2_0`, then this query would return `DML_FEATURE_LEVEL_2_0`, which is lower than the true feature level (3_0) supported by the device.

## Availability
This API was introduced in DirectML version `1.1.0`.

## -see-also

[IDMLDevice::CheckFeatureSupport method](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)

[DML_FEATURE enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)

[DML_FEATURE_QUERY_FEATURE_LEVELS structure](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
