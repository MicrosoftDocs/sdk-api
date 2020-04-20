---
UID: NF:directml.IDMLDispatchable.GetBindingProperties
title: IDMLDispatchable::GetBindingProperties
description: Retrieves the binding properties for a dispatchable object (an operator initializer, or a compiled operator).helpviewer_keywords: ["GetBindingProperties","GetBindingProperties method","GetBindingProperties method","IDMLDispatchable interface","IDMLDispatchable interface","GetBindingProperties method","IDMLDispatchable.GetBindingProperties","IDMLDispatchable::GetBindingProperties","direct3d12.idmldispatchable_getbindingproperties","directml/IDMLDispatchable::GetBindingProperties"]
old-location: direct3d12\idmldispatchable_getbindingproperties.htm
tech.root: direct3d12
ms.assetid: 537C84C0-55BD-494D-812A-728D73B93061
ms.date: 12/5/2018
ms.keywords: GetBindingProperties, GetBindingProperties method, GetBindingProperties method,IDMLDispatchable interface, IDMLDispatchable interface,GetBindingProperties method, IDMLDispatchable.GetBindingProperties, IDMLDispatchable::GetBindingProperties, direct3d12.idmldispatchable_getbindingproperties, directml/IDMLDispatchable::GetBindingProperties
f1_keywords:
- directml/IDMLDispatchable.GetBindingProperties
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDispatchable.GetBindingProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLDispatchable::GetBindingProperties


## -description







Retrieves the binding properties for a dispatchable object (an operator initializer, or a compiled operator). The binding properties
       value contains the required size of the binding table in descriptors, as well as the required size in bytes of the
       temporary and persistent resources required to execute this object.

When called on an operator initializer, the binding properties of the object may be different if retrieved both before and after a call
        to [IDMLOperatorInitializer::Reset](/windows/desktop/api/directml/nf-directml-idmloperatorinitializer-reset).


## -parameters






## -returns



Type: [**DML_BINDING_PROPERTIES**](/windows/desktop/api/directml/ns-directml-dml_binding_properties)

A [DML_BINDING_PROPERTIES](/windows/desktop/api/directml/ns-directml-dml_binding_properties) value containing binding properties.




## -see-also




<a href="/windows/desktop/direct3d12/dml-binding">Binding in DirectML</a>



[IDMLDispatchable](/windows/desktop/api/directml/nn-directml-idmldispatchable)
 

 

