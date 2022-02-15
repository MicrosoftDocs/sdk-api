---
UID: NS:directml.DML_BINDING_PROPERTIES
title: DML_BINDING_PROPERTIES
description: Contains information about the binding requirements of a particular compiled operator, or operator initializer. This struct is retrieved from IDMLDispatchable::GetBindingProperties.
helpviewer_keywords: ["DML_BINDING_PROPERTIES","DML_BINDING_PROPERTIES structure","direct3d12.dml_binding_properties","directml/DML_BINDING_PROPERTIES"]
old-location: direct3d12\dml_binding_properties.htm
tech.root: directml
ms.assetid: 000A1236-A557-4DCD-8A25-23AA5CF29C2D
ms.date: 12/5/2018
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
 - DML_BINDING_PROPERTIES
 - directml/DML_BINDING_PROPERTIES
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
 - DML_BINDING_PROPERTIES
---

## -description

Contains information about the binding requirements of a particular compiled operator, or operator initializer. This struct is retrieved from [IDMLDispatchable::GetBindingProperties](/windows/win32/api/directml/nf-directml-idmldispatchable-getbindingproperties).

## -struct-fields

### -field RequiredDescriptorCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The minimum size, in descriptors, of the binding table required for a particular dispatchable object (an operator initializer, or a compiled operator).

### -field TemporaryResourceSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

The minimum size in bytes of the temporary resource that must be bound to the binding table for a particular dispatchable
      object. A value of zero means that a temporary resource is not required.

### -field PersistentResourceSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

The minimum size in bytes of the persistent resource that must be bound to the binding table for a particular
      dispatchable object. Persistent resources must be supplied during initialization of a compiled operator (where it
      is bound as an output of the operator initializer) as well as during execution. A value of zero means that a
      persistent resource is not required. Only compiled operators have persistent resources—operator initializers
      always return a value of 0 for this member.

## -see-also

<a href="/windows/ai/directml/dml-binding">Binding in DirectML</a>
