---
UID: NF:inked._IInkEditEvents_Invoke
tech.root: tablet
title: _IInkEditEvents_Invoke
ms.date: 02/07/2023
targetos: Windows
description: Provides access to properties and methods exposed by the object.
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
 - _IInkEditEvents_Invoke
f1_keywords:
 - _IInkEditEvents_Invoke
 - inked/_IInkEditEvents_Invoke
dev_langs:
 - c++
helpviewer_keywords:
 - _IInkEditEvents_Invoke
---

# IInkEditEvents_Invoke function

## -description

Provides access to properties and methods exposed by the object.

## -parameters

### -param This

The [IInkEditEvents interface](nn-inked-_iinkeditevents.md) object.

### -param dispIdMember

Identifier of the member. Use [IInkEditEvents_GetIDsOfNames](nf-inked-_iinkeditevents_getidsofnames.md) to obtain the dispatch identifier.

### -param riid

Reserved for future use. Must be IID_NULL.

### -param lcid

Locale context in which to interpret arguments.

### -param wFlags

Flags describing the context of the call.

### -param pDispParams

Pointer to a **DIPPARAMS** structure that contains the arguments.

### -param pVarResult

Pointer to a **VARIANT** that receives the result, or **NULL** if the caller expects no result.

### -param pExcepInfo

Pointer to a structure that receives exception information.

### -param puArgErr

Pointer to a variable that receives the index of the first argument that causes an error.

## -remarks

## -see-also
