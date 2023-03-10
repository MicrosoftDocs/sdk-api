---
UID: NE:directml.DML_INTERPOLATION_MODE
title: DML_INTERPOLATION_MODE
description: Defines constants that specify a mode for the DirectML upsample 2-D operator (as described by the DML_UPSAMPLE_2D_OPERATOR_DESC structure).
helpviewer_keywords: ["DML_INTERPOLATION_MODE","DML_INTERPOLATION_MODE enumeration","DML_INTERPOLATION_MODE_LINEAR","DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR","direct3d12.dml_interpolation_mode","directml/DML_INTERPOLATION_MODE","directml/DML_INTERPOLATION_MODE_LINEAR","directml/DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR"]
old-location: direct3d12\dml_interpolation_mode.htm
tech.root: directml
ms.assetid: E6A2F4EF-4BF3-4F1B-8D0D-D3EDBD07C042
ms.date: 12/5/2018
ms.keywords: DML_INTERPOLATION_MODE, DML_INTERPOLATION_MODE enumeration, DML_INTERPOLATION_MODE_LINEAR, DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR, direct3d12.dml_interpolation_mode, directml/DML_INTERPOLATION_MODE, directml/DML_INTERPOLATION_MODE_LINEAR, directml/DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR
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
 - DML_INTERPOLATION_MODE
 - directml/DML_INTERPOLATION_MODE
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
 - DML_INTERPOLATION_MODE
---

## -description

Defines constants that specify a mode for the DirectML upsample 2-D operator (as described by the [DML_UPSAMPLE_2D_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_upsample_2d_operator_desc) structure).

## -enum-fields

### -field DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR

Specifies the nearest-neighbor mode.

### -field DML_INTERPOLATION_MODE_LINEAR

Specifies a linear (including bilinear, trilinear, etc.) mode.

## -see-also

* [DML_UPSAMPLE_2D_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_upsample_2d_operator_desc)
