---
UID: NF:ocidl.IPersistPropertyBag.Save
tech.root: com
title: IPersistPropertyBag::Save
ms.date: 05/25/2021
targetos: Windows
description: Instructs the object to save its properties to the given property bag, and optionally, to clear the object's dirty flag.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ocidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - ocidl.h
api_name:
 - IPersistPropertyBag::Save
f1_keywords:
 - IPersistPropertyBag::Save
 - ocidl/IPersistPropertyBag::Save
dev_langs:
 - c++
---

## -description

Instructs the object to save its properties to the given property bag, and optionally, to clear the object's dirty flag.

## -parameters

### -param pPropBag

The address of the caller's property bag, through which the object can write properties. This cannot be NULL.

### -param fClearDirty

A flag indicating whether the object should clear its dirty flag when the "Save" operation is complete. TRUE means clear the flag, and FALSE means leave the flag unaffected. FALSE is used when the caller performs a "Save Copy As" operation.

### -param fSaveAllProperties

A flag indicating whether the object should save all its properties (TRUE), or save only those properties that have changed from the default value (FALSE).

## -returns

## -remarks

The caller can request that the object save all properties, or save only those properties that have changed.

E_NOTIMPL is not a valid return code, because any object that implements this interface must support the entire functionality of the interface.

## -see-also

