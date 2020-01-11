---
UID: NS:directml.DML_OPERATOR_DESC
title: DML_OPERATOR_DESC
description: A generic container for an operator description. You construct DirectML operators using the parameters specified in this struct. See IDMLDevice::CreateOperator for additional details.
old-location: direct3d12\dml_operator_desc.htm
tech.root: direct3d12
ms.assetid: F6D00361-9C08-497E-BA6B-3500376966CB
ms.date: 12/5/2018
ms.keywords: DML_OPERATOR_DESC, DML_OPERATOR_DESC structure, direct3d12.dml_operator_desc, directml/DML_OPERATOR_DESC
f1_keywords:
- directml/DML_OPERATOR_DESC
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
- DML_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_OPERATOR_DESC structure


## -description






A generic container for an operator description. You construct DirectML operators using the parameters specified
    in this struct. See [IDMLDevice::CreateOperator](/windows/desktop/api/directml/nf-directml-idmldevice-createoperator) for additional details.


## -struct-fields




### -field Type

Type: [**DML_OPERATOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_operator_type)

The type of the operator description. See <a href="https://msdn.microsoft.com/2D66A3DB-FE61-4EC2-B626-DD008FF14802">DML_OPERATOR_TYPE</a> for the available types.


### -field Desc

Type: <b>const void*</b>

A pointer to the operator description. The type of the pointed-to struct must match the value specified in <i>Type.</i>

