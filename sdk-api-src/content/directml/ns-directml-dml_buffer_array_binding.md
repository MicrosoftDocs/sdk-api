---
UID: NS:directml.DML_BUFFER_ARRAY_BINDING
title: DML_BUFFER_ARRAY_BINDING
description: Specifies a resource binding that is an array of individual buffer bindings.
old-location: direct3d12\dml_buffer_array_binding.htm
tech.root: direct3d12
ms.assetid: F9634FE6-6386-4420-BC4A-EC7F140B830C
ms.date: 12/5/2018
ms.keywords: DML_BUFFER_ARRAY_BINDING, DML_BUFFER_ARRAY_BINDING structure, direct3d12.dml_buffer_array_binding, directml/DML_BUFFER_ARRAY_BINDING
ms.topic: struct
f1_keywords:
- directml/DML_BUFFER_ARRAY_BINDING
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
- DML_BUFFER_ARRAY_BINDING
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_BUFFER_ARRAY_BINDING structure


## -description






Specifies a resource binding that is an array of individual buffer bindings.


## -struct-fields




### -field BindingCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of individual buffer ranges to bind to this slot. This field determines the size of the <i>Bindings</i> array.


### -field Bindings

Type: <b>const [DML_BUFFER_BINDING](/windows/desktop/api/directml/ns-directml-dml_buffer_binding)*</b>

The individual buffer ranges to bind.


## -see-also




<a href="/windows/desktop/direct3d12/dml-binding">Binding in DirectML</a>
 

 

