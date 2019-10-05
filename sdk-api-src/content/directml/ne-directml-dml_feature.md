---
UID: NE:directml.DML_FEATURE
title: DML_FEATURE
author: windows-sdk-content
description: Defines a set of optional features and capabilities that can be queried from the DirectML device.
old-location: direct3d12\dml_feature.htm
tech.root: direct3d12
ms.assetid: 133FAC75-F745-423D-9CC6-AABB0404C036
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_FEATURE, DML_FEATURE enumeration, DML_FEATURE_TENSOR_DATA_TYPE_SUPPORT, direct3d12.dml_feature, directml/DML_FEATURE, directml/DML_FEATURE_TENSOR_DATA_TYPE_SUPPORT
ms.topic: enum
f1_keywords: 
 - "directml/DML_FEATURE"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_FEATURE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_FEATURE enumeration


## -description






Defines a set of optional features and capabilities that can be queried from the DirectML device. See [IDMLDevice::CheckFeatureSupport](/windows/desktop/api/directml/nf-directml-idmldevice-checkfeaturesupport).


## -enum-fields




### -field DML_FEATURE_TENSOR_DATA_TYPE_SUPPORT

Allows querying for tensor data type support. The query type is [DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT](/windows/desktop/api/directml/ns-directml-dml_feature_query_tensor_data_type_support), and
      the support data type is [DML_FEATURE_DATA_TENSOR_DATA_TYPE_SUPPORT](/windows/desktop/api/directml/ns-directml-dml_feature_data_tensor_data_type_support).


## -see-also




[IDMLDevice::CheckFeatureSupport](/windows/desktop/api/directml/nf-directml-idmldevice-checkfeaturesupport)
 

 

