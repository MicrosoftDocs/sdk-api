---
UID: NF:inked._IInkEditEvents_GetTypeInfo
tech.root: tablet
title: _IInkEditEvents_GetTypeInfo
ms.date: 02/07/2023
targetos: Windows
description: Retrieves the type information for the object, which can then be used to get the type information for an interface.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: inked.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - inked.h
api_name:
 - _IInkEditEvents_GetTypeInfo
f1_keywords:
 - _IInkEditEvents_GetTypeInfo
 - inked/_IInkEditEvents_GetTypeInfo
dev_langs:
 - c++
helpviewer_keywords:
 - _IInkEditEvents_GetTypeInfo
---

# IInkEditEvents_GetTypeInfo function

## -description

Retrieves the type information for the object, which can then be used to get the type information for an interface.

## -parameters

### -param This

The [IInkEditEvents interface](nn-inked-_iinkeditevents.md) object.

### -param iTInfo

Type information to return. Must be zero.

### -param lcid

Locale identifier.

### -param ppTInfo

Address of a variable that receives an ITypeInfo pointer.

## -remarks

## -see-also
