---
UID: NE:directml.DML_TENSOR_TYPE
title: DML_TENSOR_TYPE
description: Identifies a type of tensor description.
helpviewer_keywords: ["DML_TENSOR_TYPE","DML_TENSOR_TYPE enumeration","DML_TENSOR_TYPE_BUFFER","DML_TENSOR_TYPE_INVALID","direct3d12.dml_tensor_type","directml/DML_TENSOR_TYPE","directml/DML_TENSOR_TYPE_BUFFER","directml/DML_TENSOR_TYPE_INVALID"]
old-location: direct3d12\dml_tensor_type.htm
tech.root: directml
ms.assetid: 954549FD-70C4-42D7-99C9-8AE33304CDBE
ms.date: 12/5/2018
ms.keywords: DML_TENSOR_TYPE, DML_TENSOR_TYPE enumeration, DML_TENSOR_TYPE_BUFFER, DML_TENSOR_TYPE_INVALID, direct3d12.dml_tensor_type, directml/DML_TENSOR_TYPE, directml/DML_TENSOR_TYPE_BUFFER, directml/DML_TENSOR_TYPE_INVALID
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
 - DML_TENSOR_TYPE
 - directml/DML_TENSOR_TYPE
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
 - DML_TENSOR_TYPE
---

## -description

Identifies a type of tensor description.

## -enum-fields

### -field DML_TENSOR_TYPE_INVALID

Indicates an unknown tensor description type. This value is never valid.

### -field DML_TENSOR_TYPE_BUFFER

Indicates a tensor description that is represented by a Direct3D 12 buffer. The corresponding struct type is [DML_BUFFER_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_buffer_tensor_desc).
