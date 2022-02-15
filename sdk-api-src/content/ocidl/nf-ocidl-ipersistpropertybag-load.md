---
UID: NF:ocidl.IPersistPropertyBag.Load
tech.root: com
title: IPersistPropertyBag::Load
ms.date: 05/25/2021
targetos: Windows
description: Instructs the object to initialize itself using the properties available in the property bag, and to notify the provided error log object when errors occur.
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
 - IPersistPropertyBag::Load
f1_keywords:
 - IPersistPropertyBag::Load
 - ocidl/IPersistPropertyBag::Load
dev_langs:
 - c++
---

## -description

Instructs the object to initialize itself using the properties available in the property bag, and to notify the provided error log object when errors occur.

## -parameters

### -param pPropBag

The address of the caller's property bag, through which the object can read properties. This cannot be NULL.

### -param pErrorLog

The address of the caller's error log, in which the object stores any errors that occur during initialization. This can be NULL; in which case, the caller does not receive errors.

## -returns

## -remarks

All property loading must take place in the **IPersistPropertyBag::Load** function call, because the object cannot hold the IPropertyBag pointer.

E_NOTIMPL is not a valid return code, because any object that implements this interface must support the entire functionality of the interface.

## -see-also

