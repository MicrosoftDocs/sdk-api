---
UID: NF:ntdef.CONTAINING_RECORD
tech.root: 
title: CONTAINING_RECORD
description: The CONTAINING_RECORD macro returns the base address of an instance of a structure given the type and the address of a field within the containing structure.
ms.date: 08/03/2022
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ntdef.h
req.idl: 
req.include-header: 
req.irql: Any level
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ntdef.h
api_name:
 - CONTAINING_RECORD
f1_keywords:
 - CONTAINING_RECORD
 - ntdef/CONTAINING_RECORD
dev_langs:
 - c++
---

## -description

The **CONTAINING_RECORD** macro returns the base address of an instance of a structure given the type of the structure and the address of a field within the containing structure.

## -parameters

### -param address

[in]
A pointer to a field in an instance of a structure of type _Type_.

### -param type

[in]
The name of the type of the structure whose base address is to be returned.

### -param field

[in]
The name of the field pointed to by _Address_ and which is contained in a structure of type _Type_.

## -remarks

Returns a PCHAR containing the address of the base of the structure containing _Field_.

Called to determine the base address of a structure whose type is known when the caller has a pointer to a field inside such a structure. This macro is useful for symbolically accessing other fields in a structure of known type.
