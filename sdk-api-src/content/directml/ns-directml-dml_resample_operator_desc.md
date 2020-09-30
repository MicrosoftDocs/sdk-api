---
UID: NS:directml.DML_RESAMPLE_OPERATOR_DESC
title: DML_RESAMPLE_OPERATOR_DESC
description: Describes a DirectML operator that resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size.
tech.root: directml
ms.date: 01/31/2020
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
 - DML_RESAMPLE_OPERATOR_DESC
f1_keywords:
 - DML_RESAMPLE_OPERATOR_DESC
 - directml/DML_RESAMPLE_OPERATOR_DESC
---

## -description

Describes a DirectML operator that resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size. You can use a linear or nearest neighbor interpolation mode. The operator supports interpolation across multiple dimensions, not just 2D. So you can keep the same spatial size, but interpolate across channels or across batches.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

### -field InterpolationMode

Type: [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode)

The interpolation mode to use for the upsample. You can use the default value of [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode).

### -field ScaleCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The size of the <i>Scales</i> array.

### -field Scales

Type: **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***

A pointer to a constant array of **FLOAT** containing the scale factors.

## -remarks

## -see-also

