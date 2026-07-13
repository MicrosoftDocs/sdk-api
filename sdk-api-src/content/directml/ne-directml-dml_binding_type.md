---
UID: NE:directml.DML_BINDING_TYPE
title: DML_BINDING_TYPE
description: Defines constants that specify the nature of the resource(s) referred to by a binding description (a DML_BINDING_DESC structure).
helpviewer_keywords: ["DML_BINDING_TYPE","DML_BINDING_TYPE enumeration","DML_BINDING_TYPE_BUFFER","DML_BINDING_TYPE_BUFFER_ARRAY","DML_BINDING_TYPE_NONE","direct3d12.dml_binding_type","directml/DML_BINDING_TYPE","directml/DML_BINDING_TYPE_BUFFER","directml/DML_BINDING_TYPE_BUFFER_ARRAY","directml/DML_BINDING_TYPE_NONE"]
old-location: direct3d12\dml_binding_type.htm
tech.root: directml
ms.assetid: 9FAE821A-9853-41E3-9F11-A4B88498BA68
ms.date: 12/5/2018
ms.keywords: DML_BINDING_TYPE, DML_BINDING_TYPE enumeration, DML_BINDING_TYPE_BUFFER, DML_BINDING_TYPE_BUFFER_ARRAY, DML_BINDING_TYPE_NONE, direct3d12.dml_binding_type, directml/DML_BINDING_TYPE, directml/DML_BINDING_TYPE_BUFFER, directml/DML_BINDING_TYPE_BUFFER_ARRAY, directml/DML_BINDING_TYPE_NONE
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
 - DML_BINDING_TYPE
 - directml/DML_BINDING_TYPE
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
 - DML_BINDING_TYPE
---

## -description

Defines constants that specify the nature of the resource(s) referred to by a binding description (a [DML_BINDING_DESC](./ns-directml-dml_binding_desc.md) structure).

## -enum-fields

### -field DML_BINDING_TYPE_NONE

Indicates that no resources are to be bound.

### -field DML_BINDING_TYPE_BUFFER

Specifies a binding that binds a single buffer to the binding table. The corresponding binding desc type is <a href="/windows/win32/api/directml/ns-directml-dml_buffer_binding">DML_BUFFER_BINDING</a>.

### -field DML_BINDING_TYPE_BUFFER_ARRAY

Specifies a binding that binds an array of buffers to the binding table. The corresponding binding desc type is <a href="/windows/win32/api/directml/ns-directml-dml_buffer_array_binding">DML_BUFFER_ARRAY_BINDING</a>.

## -see-also

[Binding in DirectML](/windows/ai/directml/dml-binding), [DML_BINDING_DESC](./ns-directml-dml_binding_desc.md)