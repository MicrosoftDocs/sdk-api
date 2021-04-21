---
UID: NE:directml.DML_FEATURE
title: DML_FEATURE
description: Defines a set of optional features and capabilities that can be queried from the DirectML device.
helpviewer_keywords: ["DML_FEATURE","DML_FEATURE enumeration","DML_FEATURE_TENSOR_DATA_TYPE_SUPPORT","direct3d12.dml_feature","directml/DML_FEATURE","directml/DML_FEATURE_TENSOR_DATA_TYPE_SUPPORT"]
old-location: direct3d12\dml_feature.htm
tech.root: directml
ms.assetid: 133FAC75-F745-423D-9CC6-AABB0404C036
ms.date: 10/30/2018
req.header: directml.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DML_FEATURE
 - directml/DML_FEATURE
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
 - DML_FEATURE
---

## -description

Defines a set of optional features and capabilities that can be queried from the DirectML device. See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).

## -enum-fields

### -field DML_FEATURE_TENSOR_DATA_TYPE_SUPPORT

Allows querying for tensor data type support. The query type is [DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT](/windows/win32/api/directml/ns-directml-dml_feature_query_tensor_data_type_support), and the support data type is [DML_FEATURE_DATA_TENSOR_DATA_TYPE_SUPPORT](/windows/win32/api/directml/ns-directml-dml_feature_data_tensor_data_type_support).

### -field DML_FEATURE_FEATURE_LEVELS

Allows querying for the feature levels supported by the device. The query type is [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels), and the support data type is [DML_FEATURE_DATA_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_data_feature_levels).

## -see-also

* [IDMLDevice::CheckFeatureSupport method](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)
* [DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT](/windows/win32/api/directml/ns-directml-dml_feature_query_tensor_data_type_support)
* [DML_FEATURE_DATA_TENSOR_DATA_TYPE_SUPPORT](/windows/win32/api/directml/ns-directml-dml_feature_data_tensor_data_type_support)
* [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
* [DML_FEATURE_DATA_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_data_feature_levels)
