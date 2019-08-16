---
UID: NE:directml.DML_CONVOLUTION_DIRECTION
title: DML_CONVOLUTION_DIRECTION
author: windows-sdk-content
description: Defines constants that specify a direction for the DirectML convolution operator (as described by the DML_CONVOLUTION_OPERATOR_DESC structure).
old-location: direct3d12\dml_convolution_direction.htm
tech.root: direct3d12
ms.assetid: C83ED146-21DF-434B-837E-5292DABF33ED
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_CONVOLUTION_DIRECTION, DML_CONVOLUTION_DIRECTION enumeration, DML_CONVOLUTION_DIRECTION_BACKWARD, DML_CONVOLUTION_DIRECTION_FORWARD, direct3d12.dml_convolution_direction, directml/DML_CONVOLUTION_DIRECTION, directml/DML_CONVOLUTION_DIRECTION_BACKWARD, directml/DML_CONVOLUTION_DIRECTION_FORWARD
ms.topic: enum
f1_keywords: 
 - "directml/DML_CONVOLUTION_DIRECTION"
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
 - DML_CONVOLUTION_DIRECTION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_CONVOLUTION_DIRECTION enumeration

## -description

Defines constants that specify a direction for the DirectML convolution operator (as described by the [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc) structure).

## -enum-fields

### -field DML_CONVOLUTION_DIRECTION_FORWARD

Indicates a forward convolution.

### -field DML_CONVOLUTION_DIRECTION_BACKWARD

Indicates a backward convolution. Backward convolution is also known as <em>transposed</em> convolution.

## -see-also

[DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)