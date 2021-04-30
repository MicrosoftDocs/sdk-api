---
UID: NS:directml.DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT
title: DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT
description: Used to query a DirectML device for its support for a particular data type within tensors.
helpviewer_keywords: ["DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT","DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT structure","direct3d12.dml_feature_query_tensor_data_type_support","directml/DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT"]
old-location: direct3d12\dml_feature_query_tensor_data_type_support.htm
tech.root: directml
ms.assetid: 39C3FB05-E2B9-46FA-9D0F-9FCC6664B390
ms.date: 12/5/2018
ms.keywords: DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT, DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT structure, direct3d12.dml_feature_query_tensor_data_type_support, directml/DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT
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
 - DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT
 - directml/DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT
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
 - DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT
---

# DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT structure


## -description

Used to query a DirectML device for its support for a particular data type within tensors. See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport). The query type is <b>DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT</b>, and
      the support data type is [DML_FEATURE_DATA_TENSOR_DATA_TYPE_SUPPORT](/windows/win32/api/directml/ns-directml-dml_feature_data_tensor_data_type_support).

## -struct-fields

### -field DataType

Type: [**DML_TENSOR_DATA_TYPE**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)

The data type about which you're querying for support.
