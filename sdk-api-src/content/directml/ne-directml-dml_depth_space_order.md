---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Defines constants controlling the transform applied in the DirectML operators [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) and **DML_OPERATOR_SPACE_TO_DEPTH1**.
tech.root: directml
ms.date: 10/29/2020
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
 - DML_DEPTH_SPACE_ORDER
 - directml/DML_DEPTH_SPACE_ORDER
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
 - DML_DEPTH_SPACE_ORDER
---

## -description

Defines constants controlling the transform applied in the DirectML operators [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) and **DML_OPERATOR_SPACE_TO_DEPTH1**. These are used within the [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_depth_to_space1_operator_desc) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth1_operator_desc) structures.

## -enum-fields

### -field DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW

Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_depth_to_space1_operator_desc) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth1_operator_desc) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.

- **Depth version**: [Batch, (BlockHeight, BlockWidth, Channels), Height, Width]
- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]

### -field DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH

Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_depth_to_space1_operator_desc) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth1_operator_desc) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.

- **Depth version**: [Batch, (Channels, BlockHeight, BlockWidth), Height, Width]
- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]

## -remarks

See [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_depth_to_space1_operator_desc) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth1_operator_desc) documentation for examples showing the effect of these values.

## -see-also
* [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_depth_to_space1_operator_desc)
* [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth1_operator_desc)

## Availability
This enumeration was introduced in `DML_FEATURE_LEVEL_2_1`.
